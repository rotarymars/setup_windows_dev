# install VisualStudio

## Visual Studio　のインストール

[Visual Studio](https://visualstudio.microsoft.com/ja/) から　Visual Studio community editionのインストールをする。
C++ の項目は必ずチェックを入れる。

## anacondaを入れておく

anacondaを入れておく
scoop からだとエラーが出て入れられないのでanacondaを別でダウンロードして入れておく

以下はエラーが出てしまう

```bash
scoop install anaconda3
```

## scoop　のインストールと必要なツールのインストール

scoopのインストールを行う。

```bash
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
iwr -useb get.scoop.sh | iex
```

必要なアプリケーションをインストールする

```bash
scoop install git less llvm mingw unxutils
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

## install fonts

```bash
cd /c/local
git clone https://github.com/powerline/fonts.git
```

SourceCodePro ディレクトリ内の *.otf をすべて選んで、右クリックからインストール



# reference
msys2のコンソールをセットアップする

https://www.ncaq.net/2020/11/10/15/40/08/
