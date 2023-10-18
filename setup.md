# install VisualStudio

## Visual Studio　のインストール

[Visual Studio](https://visualstudio.microsoft.com/ja/) から　Visual Studio community editionのインストールをする。
C++ の項目は必ずチェックを入れる。

## scoop　のインストールと必要なツールのインストール

scoopのインストールを行う。

```bash
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
iwr -useb get.scoop.sh | iex
```

必要なアプリケーションをインストールする

```bash
scoop install git llvm mingw msys2 unxutils anaconda3
```

Visual Studio Code　をインストールする

```bash
scoop bucket add extras
scoop install vscode
```

## register git bash here
エクスプローラのパスに

%HOMEPATH%\scoop\apps\git\current

を入力。
表示されたフォルダの
install-context.reg
をダブルクリックする。


## set up atcoder library
open git bash

```bash
cd /c
mkdir -p local/lib
cd local/lib
git clone https://github.com/atcoder/ac-library.git
```

## set up online judgement tools
open git bash

```bash
cd /c
mkdir -p local
cd local

source ~/anaconda3/Scripts/activate
python -m venv oj_env
source /c/local/oj_env/Scripts/activate
pip3 install online-judge-tools
```


# reference
msys2のコンソールをセットアップする

https://www.ncaq.net/2020/11/10/15/40/08/
