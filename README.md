# RL-GSPG
grid sampling policy gradient

I am experimenting a bit with off-policy actor-critic methods for continuous control problems.
In this experiment, I use grid sampling in the action value space to define the exploration policy.
This appears a more 'natural' form of exploratory behavior compared to DDPG.
In DDPG, we add some pre-defined random process (with hand-designed parameters) to the target policy to obtain exploration.
Here, exploration instead explicitly depends on current belief of what actions might be good.

Solves the `'LunarLanderContinuous-v2'` environment task in a few hundred epsisodes:
![](https://github.com/steevsteev/RL-GSPG/blob/master/assets/learning_curve.png)

**WARNING** github seems to have problems rendering .ipynb files (including my notebook), so use this link to view the main.ipynb: https://nbviewer.jupyter.org/github/shish/RL-GSPG/blob/master/main.ipynb

## Requirements
* Python 3
* PyTorch
* CUDA support (can be disabled by editing the few lines in the code that contain `cuda`)
* OpenAI Gym
* the `hiddenlayer` python module for dynamic plots

## Usage
* run the notebook (main.ipynb)
