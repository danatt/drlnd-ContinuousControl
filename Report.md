**About the Task:**



**About the Agent:**
To solve this task, I've used a DDGP-Agent. I startet by implementing an agent with parameters from the original paper. 

**DDPG Hyperparameters:**

    BUFFER_SIZE = int(1e5)  # replay buffer size
    BATCH_SIZE = 128        # minibatch size
    GAMMA = 0.99            # discount factor
    TAU = 1e-3              # for soft update of target parameters
    LR_ACTOR = 1e-4         # learning rate of the actor
    LR_CRITIC = 1e-4        # learning rate of the critic
    WEIGHT_DECAY = 0        # L2 weight decay
    UPDATE_EVERY = 1        # how many steps to take before updating target networks

**Model architectures:**
  - Actor
  * hidden Layer 1: 128 units +relu activation
  * hidden Layer 2: 128 units +relu activation
  * outputlayer1: 1 unit + tanh activation
  
  - Critic
  * hidden Layer 1: 128 units +relu activation
  * hidden Layer 2: 132 units (128+size of actionspace) +relu activation
  * outputlayer1: 1 unit
  
**Ideas for Future Work:**


**Results:**
