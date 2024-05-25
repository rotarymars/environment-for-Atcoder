# 日本語のreadmeもあります
日本語のreadmeを参照
# What is this repository?
This repository is for making a envorinment to do Atcoder for windows users (mainly for C++).
# What to do
Run the command below in powershell to install scoop.
```bash
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
iwr -useb get.scoop.sh | iex
```
Add extra's bucket
```bash
scoop bucket add extras
```
Install mingw
```bash
scoop install mingw
```
Install git
```bash
scoop install git
```
Install python
```bash
scoop install python
```
Install vscode
```bash
scoop install vscode
```
Run the code below to get the [online-judge-tools](https://github.com/online-judge-tools/oj)
```bash
pip3 install git+https://github.com/online-judge-tools/oj.git
```
Login to the installed package by entering your username and passowrd for Atcoder in the prompt
```
oj l https://atcoder.jp/contests/agc001_a
```
Make a directory where you want to keep your codes in by
```bash
mkdir YOUR_DIRECTORY_NAME
```
Move to the directory you made
```bash
cd YOUR_DIRECTORY_NAME
```
Now, clone this repository and just clear everything except src directory, and oj_helper.py
```bash
git clone https://github.com/rotarymars/environment-for-Atcoder.git
```
# How to use this environment
First, make folders for each problem like the command below
```bash
cp -r src abc100_a
cd abc100_a
code .
```
Edit your main.cpp, and then, do
```bash
make
```
or
```bash
make all
```
It will submit your code(main.cpp) if the samples are all correct.
# Other features
download test case(s)
```bash
make download
```
compile with definition of _DEBUG and test
```bash
make test
```
download and submit from the designated url<br>
In oj_settings.json, put the url.