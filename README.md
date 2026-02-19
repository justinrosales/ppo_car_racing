# Car Racing Reinforcement Learning

Training autonomous agents to drive in both 2D (Gymnasium) and 3D (CARLA) environments using Stable Baselines3.

## How It Works

### The Playground
We use the **Gymnasium** API to run two environments:
1.  **2D Racing (CarRacing-v2)**: A fast, simple 2D game. Good for testing ideas quickly.
2.  **3D Simulation (carla-gym)**: A realistic city driving sim (CARLA). We wrap it so it works just like the 2D game.

### The Brain
Our agents use **Stable-Baselines3** to learn. A neural network looks at the screen and decides how to steer, accelerate, and brake.

### Typical Workflow
1.  **Configure**: Set up the environment.
2.  **Train**: Run the training loop. The car drives thousands of times to learn the track.
3.  **Visualise**: Use **TensorBoard** to see how the score improves over time.

## Project Structure

- `src/`: Code for the algorithms (PPO, A2C, etc).
- `docs/`: Guides on how to set up and run everything.

## Tech Stack
- **Gymnasium**: The standard for RL environments.
- **Stable-Baselines3**: The learning algorithms.
- **CARLA**: The 3D simulator.
- **PyTorch**: The deep learning framework.
- **TensorBoard**: The progress tracker.

## Documentation
- [**Environment Setup**](./docs/env-setup.md): How to install everything.
- [**Usage**](./docs/usage.md): How to train and test models.
- [**TensorBoard**](./docs/tensorboard.md): How to read the graphs.
