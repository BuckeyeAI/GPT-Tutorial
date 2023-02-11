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

6. Follow the install instructions on `nanoGPT`'s README.md, e.g., install the dependencies. (Note: replace `pip` with `pip3` if you intend to use Python3 instead of Python2 for your code). Use `pip3` preferrably. The code for installing `pytorch` is provided below for convenience (for macOS Ventura 13.1)
```
pip3 install torch torchvision torchaudio
```


## Trying out GPT

1. If you just want to try out a simplest character-level document completion GPT, follow the `quick start` section on `nanoGPT` [repo's](https://github.com/karpathy/nanoGPT) README page. The next steps are mainly a copy of the `quick start` instructions, with some added notes for beginners.

2. Navigate to `nanoGPT` folder, run `python3 data/shakespeare_char/prepare.py`. What it does: download the Shakespear dataset as `input.txt`, encode the text into integers, split the entire document into train/test sets, and save as separate `train.bin`, `val.bin` files.

3. (If using macOS) Edit the file `train.py` at line 72: `device = 'cpu'`, and `compile = False` at line 74. Reason: Andrej mentioned ' on macbook, do not torch compile the model'.

4. Run the training code with `python3 train.py config/train_shakespeare_char.py`. What it does: trains the GPT model on the Shakespear dataset.

> **Open Question:** How does the command line parameter `config/train_shakespeare_char.py` get read into the main `train.py` file?

> **Open Question:** The default setting on training iterations is 600,000. On a 2022 MacBook Air M2 with 8GB ram, this is likely taking 100,000 minutes, or 70 days. An A100 GPU will only take 3 minutes. What are the other alternatives? OSC (Ohio Super Computing) or AWS?

