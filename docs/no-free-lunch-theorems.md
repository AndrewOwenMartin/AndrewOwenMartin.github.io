# The No Free Lunch Theorems

The No Free Lunch (NFL) theorems are important to me because as an AI researcher they reframe the entire discipline from a search for the best algorithm to a search for an algorithm which has the least harmful trade-offs for a given problem.

Taken fully to heart, I believe they may be used to show that at least Superintelligence is impossible, and at most that General AI is impossible.

This is how the NFL theorems are introduced in my thesis.

# Introduction

> Introduced in [107] and applied to search algorithms in [109], the NFL
> theorems state that over the set of all possible search spaces, there can be
> no algorithm which performs better on average than random search. The
> implication of the NFL theorems in the context of comparing SDS variants is
> that over the set of all possible search spaces there are as many search
> spaces for which standard SDS outperforms a given variant than there are
> search spaces for which the same variant outperforms standard SDS. This claim
> can also be applied to any two variants of SDS and also to any variant of SDS
> and any other search algorithm. Given the NFL theorems, the emphasis of any
> variant should not be evaluated solely on the advantage it introduces, but
> rather the trade-off it represents, and how large the effect of the trade-off
> should be to maximise the net-gain in performance after the negative impact
> of the disadvantage is realised against the positive effect of the advantage.
> The optimal choice of variant and the associated parameters should therefore
> be considered in the context of the search space of the given task and the
> requirements of the solution.
> 
> - [107] D. H. Wolpert. "The lack of a priori distinctions between learning algorithms". In: Neural computation 8.7 (1996), pp. 1341-1390.
> - [108] D. H. Wolpert. "What the no free lunch theorems really mean; how to improve search algorithms". In: Santa Fe Institute. Vol. 7. 2012.
> - [109] D. H. Wolpert, W. G. Macready, et al. No free lunch theorems for search. Tech. rep. Technical Report SFI-TR-95-02-010, Santa Fe Institute, 1995.

Here are some choice quotes from the introduction of [107].

> [The NFL theorems] show, loosely speaking, that for any two algorithms A and
> B, there are "as many" targets for which algorithm A has lower expected OTS
> error than algorithm B as vice versa (whether one averages over training sets
> or not). In particular, such equivalence holds even if one of the algorithms
> is random guessing; there are "as many" targets for which any particular
> learning algorithm gets confused by the data and performs worse than random
> as for which it performs better. As another example of the NFL theorems, it
> is shown explicitly that A is equivalent to B when B is an algorithm that
> chooses between two hypotheses based on which disagrees more with the
> training set, and A is an algorithm that chooses based on which agrees more
> with the training set. Other NFL theorems are also derived, showing, for
> example, that there are as many priors over targets in which A beats B (i.e.,
> has lower expected error than B) as vice versa. In all this, the quotes
> presented at the beginning of this section are misleading at best. 

This is a bold statement. For all supervised learning algorithms there is a dataset for which that algorithm will perform *worse than random guessing*, and even *worse than doing the opposite of what the algorithm indicates*. A further dramatic implication comes in the next sentence, there are as many datasets whereyou should select an algorithm which perofrms the *worst* against the training set as there are datasets where you should choose the algorithm which performs the *best* against the training set.

Put another way, (and borrowing from [108, pp.3]), when desiging an algorithm it's common to select a class of problems, then to select a performance measure. At this point, a formal approach would be to 'solve' for the algorithm which will perform best given these two selections. In practise, algorithm selection is informally motivated.

# My 'bookmarks'

- [107] "The lack of a priori distinctions between learning algorithms" wolpert1996lack.pdf. ep. 5/52 pp. 1345
- [108] "What the no free lunch theorems really mean; how to improve search algorithms". wolpert2012what.pdf. ep. 9/14 (appendix)
- [109] D. H. Wolpert, W. G. Macready, et al. No free lunch theorems for search. Tech. rep. Technical Report SFI-TR-95-02-010, Santa Fe Institute, 1995.
- "No free lunch theorems for optimization" wolpert1996no-b.pdf
