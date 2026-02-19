# Car Racing RL

Training autonomous agents to drive in both 2D (Gymnasium) and 3D (CARLA) environments using Stable Baselines3.

## How it works
- **Playground**: We use the **Gymnasium** API as our standard interface for two different environments:
    - **2D (CarRacing-v2)**: A lightweight 96x96 pixel top-down racing game.
    - **3D (carla-gym)**: A high-fidelity urban driving simulation. The `carla-gym` wrapper acts as a bridge, letting the realistic CARLA simulator "speak" the Gymnasium language so we can use the same RL code for both.
- **Brain**: Agents use algorithms (PPO, A2C, DQN) from `stable-baselines3`. They use a CNN (Convolutional Neural Network) to process visual feeds and decide on steering, gas, and braking.
- **Workflow**: Wrap environment → Train (`model.learn`) → Save model (.zip) → Visualize with TensorBoard.

## Project Structure
- `src/ppo/`: PPO scripts and models for 2D racing.
- `src/a2c/`: A2C implementation for 2D racing (In-progress).
- `src/carla-gym/`: Data and logs for 3D simulation training.
- `docs/`: Setup and usage guides.

## Tech Stack
- **Gymnasium**: The API standard for RL environments.
- **CARLA**: High-fidelity 3D driving simulator.
- **Stable-Baselines3**: The RL algorithm library.
- **PyTorch**: Deep learning backend.
- **TensorBoard**: Benchmarking & visualization.

## Links
- [**Installation & Usage Guide**](./docs/usage.md)
- [**TensorBoard Workflow**](./docs/tensorboard.md)
