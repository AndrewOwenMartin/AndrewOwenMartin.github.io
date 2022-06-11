# The problem with representations

All models are wrong, some are useful. This isn't news, but it is of profound importance when changing contexts.

The problem with representations is that they must be selective in what they represent.
<span id="arg-no-full-representations">A representation which represents all aspects of an item will contain irrelevant detail and probably cost a lot to maintain.

So how do you choose what to represent, you can have a static set of features represented, this will be enough information for a set of situations. If the set of situations which will ever be encountered is covered by this set then everything is fine.
This is the approach applied with much success in well defined cases and toy problems.
Consider for example an algorithm for playing Noughts and Crosses or Tic-tac-toe, a representation of the board state, marking each square as blank, containing a nought, or containing a cross will be sufficient in all game states.

There are situations where a loss of information is considered acceptible, such as representing the suitibility of a person to ride on a fairground roller-coaster by their height alone.
There may be many mitigating factors outside of the height of the person which make them suitable to ride yet beneath the height limit, or unsuitable to ride yet above the height limit.
Nevertheless this crude representation is sufficient for the fairground oeprator, and presumably their insurance provider, though one can easily imagine some upset people who feel their ride suitibility was not fairly represented.

<span id="extra-info-in-complex-formal-systems">In situations that are well defined, yet complex, such as in a game of chess, a representation of the game state may be sufficient to encode all the information to represent the state such as to duplicate the state, yet insufficient to represent the state for the purposes of planning a strategy. Maybe it is important to see which pieces are protected or which pieces may be under threat within a single move. All may be inferred from the formal state, but these extra representations are not enough to allow the representation to be used for AI, and only for reporting of a historical game.

- Being-there vs objectivity.
When you're "there" you experoence all things outside of the object, relevant or not, and your attention and experience tells you what to attend to. When you are objective, then you must have decided what is relevant beforehand. The same stuff is represented in all cases, irrelevant stuff gets included and relevant stuff gets excluded.

## Upcoming points

- Who is the representation really for? The homunculus?
- Dennett's R2D2
- It's a question of being-there vs objectivitt.


# Footnotes
<ol>
<li><a href="#arg-no-full-representations">Strengthen the argument that representations must be selective, and cannot be fully detailed.</a></li>
<li><a href="#extra-info-in-complex-formal-systems">May not be a relevant argument here, is this really a 'representation' argument?</a></li>
</ol>
