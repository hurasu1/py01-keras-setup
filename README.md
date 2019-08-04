
# py01-keras-setup
2019/08/04現在  
keras + tensorflow + windows 10 + GPU でdeeplearningを動かせる環境をセットアップする。

## 環境構築
pythonのeditorは[**pycharm**](https://www.jetbrains.com/pycharm/)を利用する。理由は、intelliJ(pycharmを作った会社が出しているjava用のeditor)を使ったが、出来が良かったため。

## anacondaのインストール
pythonの仮想環境。

## pycharmのインストール
pycharmはanaconda-plugin版をインストールした。  
仮想環境にanacondaを利用する場合には、anaconda-plugin版を利用する。  
（ただし、自分の環境ではanacondaのインタープリターで新しいプロジェクトを作成すると、
なぜかpycharm自体がフリーズしてしまい、結局まだ使えずじまい。）

## グラボのドライバーアップデート
GTX-1050 Tiを利用している。ドライバーをアップデートする。  
[ドライバダウンロードサイト](https://www.nvidia.co.jp/Download/index.aspx?lang=jp)  
古いドライバーだと、cudaインストール時に、失敗してしまった。

## cuda系のツールのインストール
下記様々インストールが必要であるが、それぞれ対応するverが結構細かく決まっている。  
もし、ver違いをインストールしてしまった場合、動作しない可能性が高い。  
パッケージ同士のverに加えて、pythonのバージョンも関係する。

[verの対応表](https://www.tensorflow.org/install/source#common_installation_problems)  
[path等の通し方](https://www.tensorflow.org/install/gpu?hl=ja-jp#hardware_requirements)
- cuda
- cuDNN (cudaをインストールすると自動でインストールされる)
- (visual studio 2015のruntimeも必要かも？)

下記はpythonのライブラリとしてinstall
- keras
- tensorflow-gpu
```{shell}
pip install keras==<version>
pip install tensorflow-gpu==<version>
```
で実行ができる。

## その他
- pycharm上で、選択部分のコードを実行するショートカットは 　ALT+SHIFT+E　である。