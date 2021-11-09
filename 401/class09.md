# Dunder Methods
what are those methods? it it special built in methods in python, very powerful and productive, you can recognize that this is a dunder method because they start and end with __, 
like __init__ and __str__ for example.
```python
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```
## Object Initialization: __init__
it's basically like a constructor
```python
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []
```
# probability and Statistics in Python
what is probability?
in short words, it's the odds of tis happens or that, like flipping a coin, it's either a head or tail.

## From statistics to probability
Probability and statistics are related areas of mathematics which concern themselves with analyzing the relative frequency of events. Still, there are fundamental differences in the way they see the world:

Probability deals with predicting the likelihood of future events, while statistics involves the analysis of the frequency of past events.   
Probability is primarily a theoretical branch of mathematics, which studies the consequences of mathematical definitions. Statistics is primarily an applied branch of mathematics, which tries to make sense of observations in the real world.
Both subjects are important, relevant, and useful. But they are different, and understanding the distinction is crucial in properly interpreting the relevance of mathematical evidence. Many a gambler has gone to a cold and lonely grave for failing to make the proper distinction between probability and statistics.

This distinction will perhaps become clearer if we trace the thought process of a mathematician encountering her first craps game:

If this mathematician were a probabilist, she would see the dice and think ``Six-sided dice? Presumably each face of the dice is equally likely to land face up. Now assuming that each face comes up with probability 1/6, I can figure out what my chances of crapping out are.''
If instead a statistician wandered by, she would see the dice and think ``Those dice may look OK, but how do I know that they are not loaded? I'll watch a while, and keep track of how often each number comes up. Then I can decide if my observations are consistent with the assumption of equal-probability faces. Once I'm confident enough that the dice are fair, I'll call a probabilist to tell me how to play.''
In summary, probability theory enables us to find the consequences of a given ideal world, while statistical theory enables us to to measure the extent to which our world is ideal.
```python
import random
def coin_trial():
heads = 0
for i in range(100):
if random.random() <= 0.5:
heads +=1
return headsdef simulate(n):
trials = [] for i in range(n):
trials.append(coin_trial())
return(sum(trials)/n)
simulate(10)
>>> 5.4
simulate(100)
>>> 4.83
simulate(1000)
>>> 5.055
simulate(1000000)
>>> 4.999781
```
