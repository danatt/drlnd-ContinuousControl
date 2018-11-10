
**About the Agent:**

To solve this task, I've used a DDGP-Agent. I started by implementing an agent with parameters from the original paper. Trough a long period of hyperparameter tuning and testing I came up with these changes:

**decreasing buffer size:**

It was interesting to see the impact from the buffer size. I first used a buffer size of 1e6, so no experience is lost during training. this resulted in a linear learning curve, which came out around a score of 20 after 500 episodes. By decreasing the buffer size to 1e5 the memory gets constantly renewed after 100 episodes and this is where now in 2 of 3 runs the learning curve exponentially increases.

OU-Noise damping:

When the Agent reaches an average score of around 30 the learning curve was getting pretty unstable. So I implemented a Damping Factor to decrease the impact of the OU-Noise the further the agent gets to its maximum score. Also, I decreased sigma from 0.2 to 0.1.

Usage of CPU:

I trained the agent on my CPU instead of using the GPU because there is more serial computation involved. Running the code on CPU was ~30% faster for me.


**DDPG Hyperparameters:**

    BUFFER_SIZE = int(1e5)  # replay buffer size
    BATCH_SIZE = 128        # minibatch size
    GAMMA = 0.99            # discount factor
    TAU = 1e-3              # for soft update of target parameters
    LR_ACTOR = 1e-4         # learning rate of the actor
    LR_CRITIC = 1e-4        # learning rate of the critic
    WEIGHT_DECAY = 0        # L2 weight decay
    UPDATE_EVERY = 1        # how many steps to take before updating target networks

* **Model architectures:**

  Actor
  
      hidden Layer 1: 128 units +relu activation
      hidden Layer 2: 128 units +relu activation
      output Layer  : 1 unit +tanh activation
  
  Critic
  
      hidden Layer 1: 128 units +relu activation
      concat Layer  : 128 + size of actionspace(4)
      hidden Layer 2: 128 units +relu activation
      output Layer  : 1 unit
  
* **Results:**
* Environment solved after: 286 Episodes
![](/pictures/CC_training_500epsisodes.JPG)

* **Ideas for Future Work:**
    * Implement Prioritized Experience Replay from the DQN paper to further reduce training time.
    * Test different Agents like (PPO, A3C or D4PG) with second Version of the Reacher environment.

