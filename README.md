# Car Racing RL

Autonomous agents driving in 2D (Gymnasium).

## How it works
- **Environment**: **Gymnasium** API handles both:
    - **2D (CarRacing-v3)**: Fast 96x96 top-down racing.
- **Agents**: Algorithms from `stable-baselines3` (PPO, A2C) use a CNN to process video and output steering, acceleration, and braking.
- **Workflow**: Wrap environment → Train (`model.learn`) → Save model (.zip) → Monitor via TensorBoard.

## Tech Stack
- **Gymnasium**: Standard RL interface.
- **Stable-Baselines3**: RL algorithm suite.
- **PyTorch**: DL backend.
- **TensorBoard**: Metric visualization.
