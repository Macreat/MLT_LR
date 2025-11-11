# 1011Lecture

## Reinforcement Learning

back test for video games -

    -here a environrment is deployed to made actions, here obtain rewards and goals

- deep mind from google

## Machine vs Deep LEARNING

    - major difference are on features extracted

## CONTROL systems

-need a guide environment to simulate and get the agent learn

## Gymnasium

    API standard for reinforcement learning with many environments to deploy and test

### gymnasium use :

    first pip install the [static_controll] method
    then, import gym and use
    gym.env.registry.keys() to list environments

    - define a enviornment using
    env = gym.make(...)

#### CART POLE case

    -maps the distance and movements on environment
    (observation space -replace physical used on clasic control)

    -rewards : steps mades until pole doesnt fall
        - after one reward, we use the output observations and rewards to made a action that made us generate a better REWARD.

    after step, we iterate and update the observation space

    what should i do to have a better performance using the less computational process ¿? -> this has a high computational cost

    - the main idea is "Pulir las acciones" dada un comienzo

    - some environments has straight patters TO DETECT AND map the possible actions to have a better reward.

##### implement a simple strategy

    - POLICY SIMPLE ¿? (fit not conventional-> create POLICYS)
        - THIS allow us to obtain weights not for decision, instead for STRATEGIES to use.
    - EPOCHS === EPISODES.  (800.000 its a good proximity)

    on conclussion, the policy strategy, doesnt get a good performance, instead of this, we can use a NEURAL NETWORK TO MADE SOME ACTION

## Agent learning

    use reinforcement learning for a back propagation method ( humans reinforcement learning on this case  )

- its important remember that we dont fit the model to our obseravtion space, instead, we fit the environment charactheristics to our model.

AN AI is AI, si tiene memoria persistente y además, infiere mediante su entorno físico

## memroy and sequentiality

-use, e.g, the velocity (position derivate) and acceleration, give us long short term memory. ( This help us with the sequentiality, this can be modified with DATA observed )

## BELLMAN EQUATION

implement for a better performance.
