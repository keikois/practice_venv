# practice_venv
practice:PythonのVenvを、バージョンを切り替えてpushする

- Python3.10.4のVenvを作成
- Python3.9.12のVenvを作成
- Python3.8.13のVenvを作成
- Python3.7.13のVenvを作成
- Python3.6.15のVenvを作成
- Python3.10.4-02のVenvを作成
- miniconda3-4.7.12のVenvを作成
- anaconda3-2021.11のVenvを作成

## やり方
- pyenvでpythonの欲しいバージョンをインストールする
- pyenvでpythonのバージョンを切り替える
- 切り替えたバージョンでvenvを作成する。
- gitにadd、commit、pushする


---
下記のコマンドでpython3.10.4をインストールできる。
```
pyenv install 3.10.4
```
インストールできるバージョンを確認
```
pyenv install --list
```
今のpyenvのバージョンを確認
```
pyenv versions
```
```
 #出力結果
 
  system
* 2.7.13 (set by /Users/xxx/.pyenv/version)
  3.10.2
  3.10.4
* 3.9.12 (set by /Users/xxx/.pyenv/version)
```
切り替える時、初めにPython2系、次に3系を記載する。
```
pyenv global 2.7.13 3.10.4
```
切り替わっていることを確認
```
 #出力結果
 
  system
* 2.7.13 (set by /Users/xxx/.pyenv/version)
  3.10.2
* 3.10.4 (set by /Users/xxx/.pyenv/version)
  3.9.12
```
## venvを作成
```
python3 -m venv venv3.10.4
```
仮想環境をアクティベートする
```
. venv3.10.4/bin/activate
```
```
python -V
```
出力結果
Python 3.10.4
