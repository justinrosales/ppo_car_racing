# Car Racing RL

Training autonomous agents to drive in the **Gymnasium CarRacing-v2** environment using Stable Baselines3.

## How it works
- **Playground**: The project uses the **Gymnasium** toolkit to load the `CarRacing-v2` environment which provides a 96x96 pixel feed. The agent gets rewards for staying on track tiles.
- **Brain**: Deep RL algorithms (PPO, A2C) are provided by the `stable-baselines3` library and use a CNN to process the images and decide on steering, gas, and braking.
- **Workflow**: Wrap the environment → Train (`model.learn`) → Save model (.zip) → Visualize progress in TensorBoard.

## Project Structure
- `src/ppo/`: PPO training script and saved models.
- `src/a2c/`: A2C implementation (In-progress).
- `docs/`: Setup and usage guides.

## Tech Stack
- **Gymnasium**: Environment toolkit.
- **Stable-Baselines3**: RL algorithms.
- **PyTorch**: Deep learning backend.
- **TensorBoard**: Benchmarking & visualization.

## Links
- [**Installation & Usage Guide**](./docs/usage.md)
- [**TensorBoard Workflow**](./docs/tensorboard.md)
