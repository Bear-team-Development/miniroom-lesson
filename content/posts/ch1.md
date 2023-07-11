+++
author="cutebear"
title="第一節 - Python 安裝"
description="用 pyenv 安裝 Python"
+++

## 前言：

安裝 Python 是件非常簡單的事，有手就會

[macOS](#macOS)
[Windows](#Windows)
[Linux](#Linux)

<hr>

## macOS

### 第一步：安裝 Homebrew（如果已有請跳過）

要安裝 HomeBrew 其實非常簡單，只要把下面這行指令塞到終端機就好

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 第二步，安裝 pyenv

pyenv 是我目前用過最好安裝 Python 的方式，他基本上就是個可以切換版本的 Python

首先，要先 sync brew

```sh
brew update
```

然後，用 brew 安裝 pyenv

```sh
brew install pyenv
```

[pyenv 設置](#pyenv設置)

<hr>

## Windows

建議你直接去裝個 WSL 看 Linux 教學吧，不然就到[官網](https://www.python.org/)下載安裝器，這作者沒有 Windows 電腦 🤣

<hr>

## Linux

### 第一步：安裝 pyenv

Linux 要安裝 pyenv 也很簡單，只要輸入下面這行指令就好

```sh
curl https://pyenv.run | bash
```

## pyenv 設置

要設置 pyenv 很簡單，只要按照你使用的終端機來設置 config，最好全設置（除了 fish 如果你沒裝）

Bash:

```sh
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
```

Zsh:

```sh
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```

fish（請加到~/.config/fish/config.fish）:

```sh
set -Ux PYENV_ROOT $HOME/.pyenv
fish_add_path $PYENV_ROOT/bin
pyenv init - | source
```

## Python 安裝

要用 pyenv 安裝 Python 很簡單，只要輸入

```sh
pyenv install 版本號
```

## 如何選版本？

可能有些萌新會不知道要怎麼選版本比較好，這就要看你的需求

如果你沒有需要安裝套件的話，可以直接裝最新版

如果你有需要安裝套件的話，建議使用最新版本減一個中版本號
例如現在的最新版是 3.11.X，那就安裝 3.10 的最新版， pyenv 中只需要輸入 3.10 即可

如果想看最新的版本是多少，建議到 [Python 官網](https://www.python.org/downloads/)

上面寫 `Download Python 版本號` 的按鈕就是最新的版本

## 結語

拜託加入 [MiniRoom](https://discord.gg/NYPHeS5uju)，這裡太冷了
