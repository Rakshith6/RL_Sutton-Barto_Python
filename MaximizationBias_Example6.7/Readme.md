**Demonstrating the maximization bias in Q_learning and fixing it using Double-Q learning: Example 6.7**

_Implementation_

1. The bias arises due to uncertain estimates of state-action values for state 'B'. Initially some of the actions have positive q-values owing to normal sampling of rewards for these actions from reward~N(-0.1,1), but over time the q-values of all actions average out to become negative. 

2. I note here that the number of actions from B is not specified, so I have drawn curves for the following action possibilities including
the lower limit of actions i.e. one action. The simlations are run for different number of actions in B = 1 or 2 or 5 or 10 or 100.

3. The bias can be avoided in the early stages of learning using Double-Q learning.

_Results_

1. Generally with larger number of actions the true value is learnt later, leading to the persistence of the bias for longer number of episodes. 
For one action, there is a bias only in the first few episodes whereas for 100 actions the bias persists throughout all episodes.

2. The bias is avoided using Double-Q learning for any number of actions from B.
