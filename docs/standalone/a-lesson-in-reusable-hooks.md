# Summary

If you don't have time to read this, the result is that I recommend writing custom hooks as two functions. One called something like `fooHook` and the other called `useFoo`. `fooHook` takes a state variable and setter function as arguments, and `useFoo` actually instantiates one of the React hooks (probably `useState`, passes it to `fooHook` and returns the results.

This will allow you to reuse the hook functionality in other hooks, even conditionally, most notably in dynamic lists.

Here's an example using a simple counter component. 
```typescript
const counterHook(count, setCount) => {
  const increment = () => setCount(count+1)

  return {
    increment,
    count,
  }
}

const useCounter = (initCount) => {
  const [value, setValue] = React.useState(initCount)
  return counterHook(value, setValue)
}
```

# Introduction

I'm a fan of hooks, they solve the problem of having state all over the place in a very strict and opinionated way. I was learning React for about 6 months before I saw this excellent presentation. If the only effect of this post is to make you watch that presentation then I'll be happy with that.

In this article are a number of ways of using hooks from the first way you'll learn, through to a way I've only just recognised after years of using React.
1. Basic hook
2. Custom hook
3. Reimplenting the custom hook to work in a list
4. Rewriting the custom hook as a reducer for reuse
5. Rewriting the custom hook using the sytle from the reducer example.

# 1. Basic hook

The first thing you learn when writing hooks is to read and write state using the `useState` hook. As far as I'm aware, the "hello world" of hooks is a button which increments a displayed value when you click it. I'll call this `Counter`, and the a component with a bunch of these values may look something like this.

```typescript
const Counter = ({initCount}) => {

  const {count, setCount} = React.useState(initCount)

  const increment = () => setCount(count+1)

  const reset = () => setCount(initCount)

  return <div>
    <span>Count: {count}</span>
    <button onClick={increment}>Count!</button>
    <button onClick={reset}>Reset</button>
  </div>
}

const MyCounters = () => {
  return <div>
    <Counter initCount={0} />
    <Counter initCount={10} />
    <Counter initCount={100} />
  </div>
}
```

So far so good, but this has a big problem that the state of each counter cannot be read or modified in any way other than the component itself. That is, each Counter can change its own value, but nothing else can. This is a problem if you hope to use the Counter in a larger App. The most common example of this is when you need to increment more than one counter with a single click, or when you want to have a global "reset all counters" button.

So let's look at a way this can be achieved by separating the hook from the state.

# 2. Custom hook

Custom hooks sound scary, but anyone who is already using hooks is more or less already writing the same code, they just wrap it up differently.

```typescript
const useCounter = (initCount) =>{
  const {count, setCount} = React.useState(initCount)

  const increment = () => setCount(count+1)

  const reset = () => setCount(initCount)

  return {
    count,
    increment,
    reset,
  }
}
const Counter = ({count, increment, reset}) => {

  return <div>
    <span>Count: {count}</span>
    <button onClick={increment}>Count!</button>
    <button onClick={reset}>Reset</button>
  </div>
}

const MyCounters = () => {

  const zeroCounterHook = useCounter(0)
  const tenCounterHook = useCounter(10)
  const hundredCounterHook = useCounter(100)

  const resetAll = () => {
    zeroCounterHook.reset()
    tenCounterHook.reset()
    hundredCounterHook.reset()
  }

  return <div>
    <Counter {...zeroCounterHook} />
    <Counter {...tenCounterHook} />
    <Counter {...hundredCounterHook} />
    <button onClick={resetAll}>Reset all</button>
  </div>
}
```

This decoupling of the state code from the component allows us to manipulate the state in a number of ways but also allows us to have multiple components that benefit from the same hook. It also allows us to define a 'public interface' to the hook, note that `setCount`is not returned from the hook, so any developer wanting to use this code is less likely to manipulate the state in an invalid way.

This still has limitations, however, if you tried to make the component add a new `Counter` every time an "add counter" button is clicked, you will see an error in React as soon as you make a loop to call `useCounter` the right amount of times.

3. Reimplenting the custom hook to work in a list

The problem here is that we have to write a new hook which has all the features of our Counter hook and all the features of a list hook combined. It feels a but like having to start again, this is no terrible chore when we are writing a simple Counter hook, but if you are using a more complicated component, or have already implemented some elegant code for handling tricky edge cases, then this can be time consuming and inviting bugs.

```typescript
const useCounterList = (counterNum, initCountList) => {
  const [countList, setCountList] = React.useState(initCountList)

  const increment = (index) => {
    const newValue = [...countList]
    newValue[index] = newValue[index]+1
    setValue(newValue)
  }

  const reset = (index) => {
    const newValue = [...countList]
    newValue[index] = initCountList[index]+1
    setValue(newValue)
  {

  const resetAll = () =>{
    setValue(initCountList)
  }

  const addCounter = (initCount) => {
    const newValue = [...countList, initCount]
    setValue(newValue)
  }

  const removeCounter = () => {
    if(countList.length > 0){
      const newValue = [...countList].slice(countList.length-1)
      setValue(newValue)
    }
  }

  return {
    countList,
    increment,
    reset,
    resetAll,
    addCounter,
    removeCounter,
  }
}

const CounterList = ({countList, increment, reset, resetAll, addCounter, removeCounter}) => {
  return <div>
    {countList.map(
      (count, index) => <div key={index}>
        <span>Count: {count}</span>
        <button onClick={() => increment(index)}>Count!</button>
        <button onClick={() => reset(index)>Reset</button>
      </div>
    )}
    <button onClick={resetAll}>Reset all</button>
    <button onClick={addCounter}>Add counter</button>
    <button onClick={removeCounter}>Remove counter</button>
  </div>
}
```

This seems to work, but there are two problems here that always concerned me, we are basically rewriting the `useCounter` hook (not so much trouble, admittedly, but hooks can get very complicated and this means more busy work, more code to keep in sync, and more chance to introduce bugs) as well as rewriting some fairly generic list manipulating functions.

The next section shows a way to write a hook with a reducer so the code can be reused, and also introduces a generic `useList` reducer which can be used to wrap any hook written in such a way into a dynamic list.

# reducer hook example

```
counterReducer

listReducer
```

9 
 1kq 
This example immeditely looks much more complicated than the previous examples, but there are a few advantages. Firstly, by passing aroind only one setter function (the `dispatch`) you avoid a callback hell which quickly gets unmanageable if you work with nested components or, god forbid, recursive functions.

# normal hook example
