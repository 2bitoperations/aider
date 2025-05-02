# install gfortran
## `brew install gfortran llvm openblas libomp pyenv pyenv-virtualenv`
## `brew link openblas --force`
# create a python virtual environment
```bash
pyenv install 3.12
pyenv virtualenv 3.12 aider-copilot
pyenv activate aider-copilot
```
# install litellm, aider
```bash
export CC=/opt/homebrew/opt/llvm/bin/clang
export CXX=/opt/homebrew/opt/llvm/bin/clang++
pip install numpy scipy
pip install git+https://github.com/2bitoperations/litellm.git@litellm_dev_03_05_2025_contributor_prs
pip install git+https://github.com/2bitoperations/aider.git@3e924e4a230ae39d24d9b255c3cdd6320383252f
```
### NOTE: If you get an error calling out `include type_traits`, follow instructions here to blow away and reinstall xcode command line tools: https://github.com/numpy/numpy/issues/27863#issuecomment-2507195757
