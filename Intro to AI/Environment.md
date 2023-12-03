A place where the [[Agent|agent]] resides.
# Properties of Environment
## Observability
### Fully Observable 
The agent can obtain all data that are necessary for it to perform a task. (a chess game, All pieces are visible)
### Partially Observable
The agent lacks data some data and must sometimes take random actions. (a card game, players are not aware of card of others)
## Multiplicity
### Single agent
The environment contains only one agent (image recognition algorithm)
### Multiple agent
The environment contains many agents (chess game, AI vs human)
## Level of Uncertainty
### Deterministic
The next state of the environment is predicable and is known ahead of time (traffic lights, chess game, where each move can be predicted)
### Stochastic
The next state of the environment is unpredictable and involves randomness (card game, agents cannot know for sure what card would be placed next)
## Episodic v. Sequential 
### Episodic 
Actors act in an "episode" and maximize only one episode.
### Sequential
Environment states change one after the other and actors must maximize each the sum of each state.
## Changeability
### Static
Environment does not change with time (puzzle game, it has only one solution and it does not change with actions of the actor)
### Dynamic
Environment changes with time
## Discreteness
### Discrete
The environment changes in steps (chess)
### Continuous
The environment changes in like a smooth curve (real world, things happen continuously thorough time)
## Knowledge
### Known
The author of the actor understand the environment completely.
### Unknown
The author of the actor does not understand the environment completely.
# Acronym
 OMUT_CDK:
- Observability
- Multiplicity
- Uncertainty
- Timeframe
- Changability
- Discreteness
- Knowledge
