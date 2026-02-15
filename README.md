# MLops_Production_Visa

## Setting up Env with uv
1. **Initialize & Migrate:**
* `uv init`
* `uv add -r requirements.txt`
* *Why:* This automatically creates your `pyproject.toml`, populates it with your dependencies, creates the `.python-version` file, and generates the `uv.lock` file in one go.


2. **Sync (The "One-and-Done" Step):**
* `uv sync`
* *Why:* This replaces `uv venv` and `uv pip install`. It creates the virtual environment if it doesn't exist and ensures it exactly matches your lockfile.


3. **Project Packaging (The Modern Way):**
* Instead of adding `-e .` to a text file, simply ensure your `pyproject.toml` has a `[build-system]` section (added by default with `uv init`).
* To install the project in editable mode, just run `uv sync`. `uv` treats the current directory as an editable package by default if it's a project.

