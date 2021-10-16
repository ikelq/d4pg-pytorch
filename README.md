# D4PG-pytorch

PyTorch implementation of Distributed Distributional Deterministic Policy Gradients (https://arxiv.org/abs/1804.08617).
<p align="center">
<img width="554" alt="d4pg_arch" src="https://user-images.githubusercontent.com/23639048/137602300-f2763ef1-2b67-4f76-aa8b-232afaa08a23.png">
</p>
Implementation was tested on environments from OpenAI Gym.

# About
D4PG and D3PG implementations with following features
* learner, sampler and agents run in separate processes
* exploiter agent(s) exists which acts without noise in actions on target network
* GPU is hold only by exploiters, all other exploration processes are run on CPU

Project was tested on Ubuntu 18.04, Intel i5 with 4 cores, Nvidia GTX 1080Ti

# Usage
Run `train.py --config configs/d4pg/walker2d_d4pg.yml`

# Tests
`python -m unittest discover`

## Results
<img width="1253" alt="d4pg_results2" src="https://user-images.githubusercontent.com/23639048/137603098-dbc42798-af5e-4b2c-9aba-90c99b5db109.png">

## Reproduce
All results were obtained with configs in `configs` directory

## References

* Continuous control with deep reinforcement learning, [https://arxiv.org/abs/1509.02971]
* Distributed Distributional Deterministic Policy Gradients [https://arxiv.org/abs/1804.08617]
