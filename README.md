# GPT-Tutorial
Creating GPT using Python

## Installing environment and dependencies

1. (On macOS e.g., Ventura 13.1) install homebrew by:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
then set homebrew to path by
```
echo '# Set PATH, MANPATH, etc., for Homebrew.' >> /Users/tz/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/tz/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

2. Install python3 by `brew install python3`. This installs python3 to `/opt/homebrew/bin/python3`. The installation directory can be verified by running `which python3`.

3. Install the python virtual environment tool by `pip3 install virtualenv`. The installation directory can be verified by running `which virtualenv` (which should return `/opt/homebrew/bin/virtualenv`.

4. Activate the venv by `source .gpt/bin/activate`.

5. Fork or download the `nanoGPT` [repo](https://github.com/karpathy/nanoGPT) from Andrej Karpathy.

6. Follow the install instructions on `nanoGPT`'s README.md, e.g., install the dependencies. (Note: replace `pip` with `pip3` if you intend to use Python3 instead of Python2 for your code). Use `pip3` preferrably.

## Trying out GPT

1. If you just want to try out a simplest character-level document completion GPT, follow the `quick start` section on `nanoGPT` [repo's](https://github.com/karpathy/nanoGPT) README page.
