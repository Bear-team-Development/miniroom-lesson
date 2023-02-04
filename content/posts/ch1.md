+++
author="cutebear"
title="第一節 - python安裝"
description="用pyen安裝python"
+++


## 前言：

安裝python事件非常簡單的事，有手就會

[Mac OS](#MacOS)
[Windows](#Windows)
[Linux](#Linux)
<hr>

## MacOS

### 第一步：安裝Homebrew（如果已有請跳過）

要安裝HomeBrew其實非常簡單，只要把下面這行指令塞到終端機就好
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 第二步，安裝pyenv

pyenv是我目前用過最好安裝python的方式，他基本上就是個可以切換版本的python

首先，要先sync brew
```sh
brew update
```
然後，用brew安裝pyenv
```sh
brew install pyenv
```

[pyenv設置](#pyenv設置)
<hr>

## Windows
建議你直接去裝個wsl看linux教學吧，不然就到[官網](https://www.python.org/downloads/)下載安裝器，這作者沒有windows電腦🤣
<hr>


## Linux

### 第一步：安裝pyenv
linux要安裝pyenv也很簡單，只要輸入下面這行指令就好
```sh
curl https://pyenv.run | bash
```

## pyenv設置

要設置pyenv很簡單，只要按照你使用的終端機來設置config，最好全設置（除了fish如果你沒裝）

bash:
```sh
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
```

zsh:
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

## python安裝

要用pyenv安裝python很簡單，只要輸入
```sh
pyenv install 版本號
```

## 如何選版本？

可能有些萌新會不知道要怎麼選版本比較好，這就要看你的需求

如果你沒有需要安裝套件的話，可以直接裝最新版

如果你有需要安裝套件的話，建議使用最新版本減一個中版本號
例如現在的最新版是3.11.X，那就安裝3.10的最新版，pyenv中只需要輸入3.10即可

如果想看最新的版本是多少，建議到[python官網](https://www.python.org/downloads/)

上面寫 `Download Python 版本號` 的按鈕就是最新的版本


## 結語
拜託加入[MiniRoom](https://discord.gg/NYPHeS5uju)，這裡太冷了
