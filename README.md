# Udacity-proj2

[//]: # (Image References)

[image1]: https://video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif "Unity ML-Agents Reacher Environment"

### The Environment
For this project, you will work with the Reacher environment.

![Trained Agent][image1]

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.


### Solving the Environment
The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. In the case of the plot above, the environment was solved at episode 63, since the average of the average scores from episodes 64 to 163 (inclusive) was greater than +30.


### Getting Started

Download the environment from one of the links below.  You need only select the environment that matches your operating system:
- Linux: [click here](href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip")
- Mac OSX: [click here](href="href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip")
- Windows (32-bit): [click here](href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip")
- Windows (64-bit): [click here](href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip")
    
(_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

2. Place the file in the DRLND GitHub repository, in the `p2_continuous-control/` folder, and unzip (or decompress) the file. 

### Dependencies

To install the necessary packages you can:

     pip install -r /path/to/requi.txt
  
after you download the files.

### Run the code

After installing the dependencies, the reported code is ready to run in the file DDPG.ipynb.
This will train the models from scratch. If instead the user wants to load the trained files it can so by:

    agent.actor_local = torch.jit.load('actor_local.pt')
    agent.critic_local = torch.jit.load('critic_local.pt')
    
after the line:
    agent = Agent(state_size, action_size, random_seed=10)
