# 🔥 Smart Heating Controller using Reinforcement Learning

## 🚀 Overview

Traditional heating systems are typically controlled by simple thermostats, maintaining constant temperatures regardless of occupancy or time of day. This leads to **energy inefficiency** and **higher heating costs**.

This project aims to develop a **smart heating controller** using **Reinforcement Learning (RL)** with [Ray RLlib](https://ray.readthedocs.io/en/latest/index.html). By training an RL agent in a virtual environment, we enable the system to **adaptively learn** when to heat or conserve energy based on real-time conditions. The ultimate goal is to deploy this agent onto a **mini-computer** (like a Raspberry Pi) for real-world smart heating control.

---

## 🧰 Features

- 🧠 **RL-Based Heating Agent** trained using Ray RLlib
- 🌡️ **Custom OpenAI Gym Environment** simulating temperature dynamics
- 🖥️ **Simulator Interface** to visualize and test agent behavior
- 💾 **Checkpointing** and training configuration
- 🔬 **Baseline Comparisons** for performance benchmarking

---

## 📦 Usage Guide
 1. Check out this repository
 2. Set up `anaconda` environment by running 

    `conda env create -f environment.yml`

 3. Configure the simulator by setting temperature and training parameters in `heating_controller_config.py` and choose the algorithm in `heating_controller_train.py`. In the latter file, the configuration of the policies can also be adapted. Run

    `python heating_controller_train.py`

    and the checkpoints will be stored by default in `~/ray_results/heat_sim`.

 3. Run `python heating_controller_train.py` after configuring simulator (mostly setting target temperature and outside temperature) and chosing algorithm.
 4. Apply trained policy in simulator by running 

    `python heating_controller_simulate.py [Path to checkpoint] [Checkpoint nr]`

    The policy can be benchmarked against two baselines by appending `--baseline [Baseline name]` to this command.

## Results
`TODO`



