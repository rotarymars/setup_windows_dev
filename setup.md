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
scoop install git llvm mingw msys2 time unxutils
```

Visual Studio Code　をインストールする

```bash
scoop bucket add extras
scoop install vscode
```


msys2のコンソールをセットアップする

https://www.ncaq.net/2020/11/10/15/40/08/