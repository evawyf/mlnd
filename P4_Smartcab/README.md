# Train a Smartcab to Drive
This program applies reinforcement learning to build a simulated vehicle navigation agent. The task involves modeling a complex control problem in terms of limited available inputs, and designs a scheme to automatically learn an optimal driving strategy based on rewards and penalties.  
In short, it incrementally teach a smartcab how to drive through a simulated city grid following common US traffic laws, avoiding accidents with other drivers, and arriving at its destination within a specified time limit.

## Install
- Python 2.7
    + I recommend installing [Anaconda](https://www.continuum.io/downloads) as it is already set up for machine learning
    + If unfamiliar with the command line there are graphical installs for macOS, Windows, and Linux
- [pygame library](https://www.pygame.org/wiki/GettingStarted)
    + `pip install pygame`

## Run
**Command Line**  
`git clone https://github.com.com/bananuhbeatdown/smartcab`  
`python agent.py`

## Parameters
By using the options found in the `agent.py`, `environment.py`, and `simulator.py` files you can experiment with the model! In-depth option explanations can be found in [smartcab.ipynb](https://github.com/BananuhBeatDown/smartcab/blob/master/smartcab.ipynb).  
**Options listed in the order they appear in the files.*


#### agent.py
- `learning` - set to True to enable driving agent to use Q-Learning implementation
- `epsilon` - starting exploration factor of the Q-Learning algorithm
- `alpha` - learning rate of the Q-Learning algorithm

#### environment.py
- `enforcement_deadline` - set to True to enforce a deadline metric

#### simulator.py
- `update_delay` - time between each trial
- `display` - set to true to enable the visual simulation
- `log_metrics` - set to True to log the simulation results as a `.csv` file in `/logs`
- `optimized` - set to True to perform an optimized version of the Q-Learning implementation
- `tolerance` - the epsilon testing threshold
- `n_test` - set number of testing trials

## Example output
The `visuals.py` file can create performances graphs from the `.csv` files `/log` folder to you help understand the performance of your smartcab during the test simulations, and give you an overall safety and reliability rating.  
**Safety and reliability chart can also be found in the [smartcab.ipynb](https://github.com/BananuhBeatDown/smartcab/blob/master/smartcab.ipynb).*
```python
# import the visualization code
import visuals as vs
vs.plot_trials('sim_improved-learning.csv')
```
![alt text](https://user-images.githubusercontent.com/10539813/27612976-6611ae24-5b99-11e7-9262-d541392d48f6.png)

## License
The smartcab program is a public domain work, dedicated using [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). I encourage you to use it, and enhance your understanding of reinforcement learning and the machine learning concepts therein. :)

