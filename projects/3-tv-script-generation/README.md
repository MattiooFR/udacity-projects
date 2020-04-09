# TV Script Generator

The goal of this project is to generate TV script content with an Recurrent Neural Network that we trained on TV scripts dataset before.

The first step was to pre process the dataset by creating lookup table. It is dictionnaries where we can transform words to unique id and vice versa. We also transformed punctuation into words.

The next was to batch transform our training set. The idea is to have a fixed set amount of words that we feed the RNN, that is `n` and then the `n+1` word represent the target.

The RNN architecture is made of LSTM cells, dropout and embedding layers.

You can find the notebook project [here](dlnd_tv_script_generation.ipynb)

Here is an example of a generated TV Script that I find hilarious :

```text
george: oh, i got to get out of my apartment, and i was wondering...

elaine:(to george) hey.

elaine: hi...(to elaine) what is this?

george: hi, hi.

george:(to george) hey, hey, hey, hey! what is this?

jerry: oh, yeah. i think it's not a problem.

elaine:(to himself) hey, what is this?

jerry: oh!

jerry:(to george) yeah, yeah, yeah?

george:(on the speaker) oh.(hangs up his bag)

kramer:(sarcastic) no. i got to go.

jerry:(to george) what?

kramer:(to george) you know, i think you got it.

jerry:(pointing) hey, what is that?

kramer: i was gonna have a lot of money..

jerry: oh, no. no.

george: you want to get a bite?

jerry: i don't know.

george: what?

jerry: what?

elaine: i know what the guy said.

jerry: i think it wasn't a natural idea.

elaine: i don't know why i don't even think so.

george: you know what?

kramer: oh, well, i guess, i know, but i was just wondering, i think we should get that checked to be in the same.

elaine:(smiling, desperate) well, i was just curious.

elaine: i know, i was a little bit.(to jerry) hey, you know, if you're not, i have to do this, and i don't even think you should have to get in the city.

george:(to elaine) i got to go to the bathroom.

kramer:(pointing) well, i'm sorry.(kramer enters)
```
