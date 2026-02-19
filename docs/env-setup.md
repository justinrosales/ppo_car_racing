# General Environment Setup

This guide serves as a single source of truth for setting up the environment to run any RL algorithm (PPO, A2C, etc.) in this repository.

## 1. System Requirements

### Operating System
- **macOS (Apple Silicon)**: Supported and tested.
- **Linux/Windows**: Should work but may require slightly different Box2D installation steps.

### Python Version
- **Recommended**: Python **3.10** or **3.11**.
- **Supported**: Python 3.12+ (requires specific `setuptools` workaround, see below).

## 2. Installation Steps

### Step 1: Install System Dependencies (macOS)
On macOS (especially M1/M2/M3), you need `swig` to compile the Box2D physics engine.
```bash
brew install swig
```

### Step 2: Create a Virtual Environment
Always use a virtual environment to manage dependencies locally.
```bash
# Create a virtual environment named .venv
python3.10 -m venv .venv

# Activate it
source .venv/bin/activate
```
*Note: If you don't have python3.10, you can use `python3 -m venv .venv`, but be aware of the setuptools issue below.*

### Step 3: Install Python Dependencies
Install the required packages. We use `shimmy` to make the new Gymnasium library compatible with Stable-Baselines3.

```bash
pip install "gymnasium[box2d]" stable-baselines3 "shimmy[gym-v21]" tensorboard
```

### Step 4: Fix for Python 3.12+ (TensorBoard Issue)
If you are using Python 3.12 or newer, you might encounter `ModuleNotFoundError: No module named 'pkg_resources'` when running TensorBoard. This is because recent `setuptools` versions removed this module.

**Fix:** Downgrade `setuptools` to a version that still includes `pkg_resources`.
```bash
pip install "setuptools<70.0.0"
```

## 3. Verifying the Setup

To verify everything is working, you can try running one of the training scripts (e.g., PPO):
```bash
source .venv/bin/activate
python src/ppo/ppo_car_racing.py
```
If it starts training without import errors, your environment is ready!
