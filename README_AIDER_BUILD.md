# install some brew dependencies (compilers and the like)
```bash
brew install gfortran llvm openblas libomp uv python@3.11
brew link openblas --force
```
# create a python virtual environment
```bash
uv venv --python 3.11 ~/.virtualenvs/aider-venv
source ~/.virtualenvs/aider-venv/bin/activate
```
# install litellm, aider
```bash
uv pip install git+https://github.com/2bitoperations/aider.git@add_copilot
```
### NOTE: If you get an error calling out `include type_traits`, follow instructions here to blow away and reinstall xcode command line tools: https://github.com/numpy/numpy/issues/27863#issuecomment-2507195757
# run with
`uv run --active aider --model github_copilot/gemini-2.5-pro`
<br>
or
<br>
`uv run --active aider --model github_copilot/gpt-4.1`
<br>
or
<br>
`uv run --active aider --model github_copilot/gpt-5`
<br>
or
<br>
`uv run --active aider --model github_copilot/claude-3.7-sonnet-thought --thinking-tokens 32k`
