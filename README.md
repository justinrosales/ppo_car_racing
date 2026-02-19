# Car Racing RL

Autonomous agents driving in 2D (Gymnasium) and 3D (CARLA) using Stable Baselines3.

## How it works
- **Environment**: **Gymnasium** API handles both:
    - **2D (CarRacing-v3)**: Fast 96x96 top-down racing.
    - **3D (carla-gym)**: High-fidelity urban driving via CARLA integration.
- **Agents**: Algorithms from `stable-baselines3` (PPO, A2C) use a CNN to process video and output steering, acceleration, and braking.
- **Workflow**: Wrap environment → Train (`model.learn`) → Save model (.zip) → Monitor via TensorBoard.

## Structure
- `src/`: Algorithm-specific code and saved models.
- `docs/`: Technical guides and setup instructions.

## Tech Stack
- **Gymnasium**: Standard RL interface.
- **CARLA**: 3D driving simulator.
- **Stable-Baselines3**: RL algorithm suite.
- **PyTorch**: DL backend.
- **TensorBoard**: Metric visualization.

## Documentation
- [**Environment Setup**](./docs/env-setup.md)
- [**Usage Guide**](./docs/usage.md)
- [**TensorBoard Workflow**](./docs/tensorboard.md)
