
exploration
	im going to go for the (maybe less immediately rewarding) option that allows me to gather more information to try and make a better decision later
		will there ever be a better decision? in the case there isnt, you've skipped over the optimal one and you might never be able to go back. 
		MORE RISKY BC THERE MIGHT NOT NEVER BE A BETTER OPTION, IN WHICH CASE, YOU JUST CHOSE A BAD OPTION. 
	
 exploitation
	i have some knowledge to tell me that one decision might be best, so im just going to take it
		there might be a better decision some arbitrary time in the future, but at least you have a pretty good decision now. 
		SAFE APPROACH. 
yt example: recommend from user's most watched (exploit) or from random other creators (explore)
pattern: should i stay somewhere i know works well or should i try something new that might fail or be much better. 

	in one, you are going to learn a lot more. positive and negative reinforcement. 
observations drive decisions (past data) and decisions lead to new observations (new data)
	exploration optimizes for most amount of new observations based on the decision. need a lot of data to train a good model (positive and negative). but, you will have to run for a lot longer. 


**P(A)** probability that some event occurs
**agent** - person making the decisions that leads to good or bad outcomes
ex. spotify decides to make me a new playlist based on what ive already listened to plus related artists - spotify is the agent and this may have good or bad consequences (on how much i listen)
trying to find a new way home that might be shorter but more dangerous, im the agent
**action** - something the agent chooses to try to maximize a reward
**reward** - the outcome of an action (can be good or bad)
**reward distribution** - probability of the action and associated reward = probability of the reward
**expected reward** - multiply the probability of the action by the reward for that action to get the the chances of you making that reward. do that for all possible events and u get the "average" reward. if i were to play this game 1 time, on average i expect to get this. 

strategy/policy - what drives how the agent makes a decision 
update rule - update the strategy based on the results

*develop analogy using climbing*

## the multi armed bandit problem
**agent** (me) must choose which slot machine to play (**action**). each slot machine has a different **reward distribution**, aka, my **expected reward** might be higher from some over others because theres a higher probability of me winning in some. 

	`To achieve this goal, at each iteration, the agent has then to balance between the need to acquire more knowledge about the reward distributions of each of the K choices (exploration) and the need to optimise rewards based on its current knowledge (exploitation).`

i found one where i win most of the time. should i keep playing that or should i play another to see if it has higher distribution. 

notations
K - # of slot machines
t - what iteration (how many/which slots we've tried)
P(x) - success probability for a machine (3/10)

# the strat!
**greedy** - always exploit. 
update rule: average all the rewards observed for the machine thus far
did it twice, (0.5 + 1) / 2 = 0.75

estimate of success. + failure = 1

expected reward: (0.75)(1) + (0.25)(0) = 0,75
multiply the probability of the action by the reward for that action


**e-greedy**
with a greedy algorithm, we dont want to fully exploit all the time because we might miss take the action with the optimal reward. so, we add a parameter e that describes. e is probability of us taking a completely random action.


greedy strategy: might overlook the actual best case after picking a medium solution. 
e-greedy: if your e value is too high, you might explore forever. but, its great because you get to collect more data. run it for a long time. 


terms to know:
agent
action
reward
reward distribution
expected reward


climbing a rock. 
K - number of routes i can use to climb it
t - what iteration im on
P(x) - success probability for a route


route number | estimate of success | estimate of failure | reward
1 | 0.4 | 0.6 | 1
**2 | 0.3 | 0.7 | 2**
3 | 0.2 | 0.8 | 3
4 | 0.1 | 0.9 | 4

agent - me
action - which route should i try to climb
reward - making it to the top
reward distribution - based on how cool it was for me to do that
expected reward if i choose randomly- multiple probability * reward and add it up. 
0.4(1) + 0.3(2) + 0.2(3) + 0.1(4) = 0.4+0.6+0.6+0.4 = 2

expected reward if i choose 2 every time = 0.3*2 = 0.6

greedy
actual
1 | 0.4 | 0.6 | 1
**2 | 0.3 | 0.7 | 2**
3 | 0.2 | 0.8 | 3
4 | 0.1 | 0.9 | 4

observed:
intial guess:
1 | 0.5 | 0.5 | 1
**2 | 0.5 | 0.5 | 2**
3 | 0.5 | 0.5 | 3
4 | 0.5 | 0.5 | 4

greedy, i pick the one w the highest expected reward, 4. so i try it, but i fail! i do not get the reward! so i will update the estimate of success like so:
(0.5 + 0 ) / 2 = 0.25

1 | 0.5 | 0.5 | 1
**2 | 0.5 | 0.5 | 2**
3 | 0.75 | 0.5 | 3
4 | 0.25 | 0.5 | 4

greedy, i pick the one w the highest expected reward, 3. so i try it, and i make it to the top! i will update the success as such. 
0.5 + 1 /2 = 0.75

now, i will keep going up 3. i might fail more than i thought, but my expected reward is pretty good so im fine with it. unless my success dips below 0.5 (probably, bc the real is 0.3), i wont try anything else. 

e greedy
have a preset parameter e. take the action that is optimal with probability 1-e or a completeley random action 
1-e chance i take the currently best possible action
e chance i take a random option. 
choose e to be 0.2. now, try update your table 10 times, 8 of those choosing the best possible sol and 0.2 being a random one. 


the agent will again choose action 2 at time t=2 as it has the highest estimate of expected reward (0.75 > 0.5). it just has the highest estimate of success (which is what the greedy algorithm optimizes for), unles all slots have the same reward. 


industry examples of explore vs exploit
should i take a class in my major or one in a completely different one
spotify: should i recommend music based on artists a person likes or genres a person listens to. 
google maps: should i recommend a route with current traffic on it due to an accident (that might clear up by the time they get there), or a more roundabout route that initially seems longer. 



review how to manipulate tuples/lists/classes in python

tuples
	cant change their contents
	indexed, so can have duplicates
	sum, min, max, len, cmp (=)
	can convert any list to a tuple

list 
insert (element, position)
append(element) --> to end of list
extend([]) --> appends all items from variable list to original list
remove(elem) --> first item that 
pop(index) --> removes and returns 
sorted(list), from lowest to highest
set(list)
reverse
len
min max

[expression(variable) for variable in input_set [predicate][, …]]