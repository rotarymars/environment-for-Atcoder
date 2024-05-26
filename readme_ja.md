# There is an English readme too!
Please check the readme.md
# これは何のリポジトリ？
Atcoderで競技プログラミングをするための環境をWindowsで整えるためのものです(C++で書くことを想定)
# 何をすればいいか
次のコマンドをPowershellで実行し、scoopをインストールする
```bash
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
iwr -useb get.scoop.sh | iex
```
バケットの追加
```bash
scoop bucket add extras
```
mingwを入れる
```bash
scoop install mingw
```
gitを入れる
```bash
scoop install git
```
pythonを入れる
```bash
scoop install python
```
vscodeを入れる
```bash
scoop install vscode
```
[online-judge-tools](https://github.com/online-judge-tools/oj)を入れる
```bash
pip3 install git+https://github.com/online-judge-tools/oj.git
```
または
```bash
python -m pip install git+https://github.com/online-judge-tools/oj.git
```
を実行する<br>
Atcoderのユーザー名とパスワードを入れてログインする
```
oj l https://atcoder.jp/contests/agc001_a
```
作業するディレクトリを作る
```bash
mkdir YOUR_DIRECTORY_NAME
```
作業するディレクトリに移る
```bash
cd YOUR_DIRECTORY_NAME
```
git cloneでこのリポジトリをクローンし、srcディレクトリとoj_helper.py以外のものを削除する
```bash
git clone https://github.com/rotarymars/environment-for-Atcoder.git
```
# どのようにしてこの環境を使うか
各問題ごとにディレクトリを作る(下記参照)
```bash
cp -r src abc100_a
cd abc100_a
code .
```
main.cppに適切なプログラムを書き込み、
```bash
make
```
または
```bash
make all
```
を実行する<br>
サンプルがすべて通った場合、コードを提出します。
# その他の機能
サンプルのダウンロードのみ
```bash
make test
```
_DEBUGをデファインしてコンパイルし、テストする
```bash
make debugtest
```
指定したurlからサンプルを取り、提出するには、<br>
oj_settings.jsonのurlを入れることで、できる
<br><br>
ソースコードの提出のみならば、
```bash
make submit
```
で実行できる
