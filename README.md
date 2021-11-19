# 概要

GitHub Actions で reusable workflow を呼び出すサンプル。

# 制限

call-workflow を使ったやりかたにはまだ制限が多い。

* with で指定する入力項目に env を使用できない。  
  なのでユーザが入力した値を元に call-workflow を呼び出すことができない。
* uses の指定に関する制限
  * 同一リポジトリの yaml を呼び出すにも関わらず owner, repository 名を指定しないといけない。
  * @ で指定するブランチ名を可変にできない。例えば dev ブランチで呼び出した場合に dev ブランチの yaml ファイルを指定する、ができない。
