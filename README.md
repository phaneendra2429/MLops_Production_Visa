# MLops_Production_Visa

## Setting up Env with uv
- pip install uv (if not exist)
- after installed uv --version (check if exists)
- uv init
- uv venv (create virtual env)
- uv pip install -r requirements.txt (install dependencies from requirements.txt)

Once the packages are installed properly
- uv add -r requirements.txt (update requirements.txt to pyproject.toml)
- uv lock (lock the dependencies)
- uv sync (install dependencies from toml)

Creating the project package
- Update the metadata in toml file: Name
- add -e . in teh requriements.txt and enter uv pip install -r reqs.txt
- New Proejct package will be created.