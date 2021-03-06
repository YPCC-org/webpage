## WEBサイト

### 記事の編集
mkdocsを使ってページを生成しています。
``` src/docs/ ``` 内のマークダウンなどを編集することで記事の内容を編集できます  
``` docs ```フォルダは自動生成されたものなので変更しても毎回リセットされるのでいみないです。

### mkdocsの設定
``` src/mkdocs.yml ``` がmkdocsの設定ファイルです。  
[こちら](https://qiita.com/mebiusbox2/items/a61d42878266af969e3c) のサイトなどを参考に作りましたので、変更が可能です。  
MKDocs for Materialのページは[こちら](https://squidfunk.github.io/mkdocs-material/)です。

### ローカル環境での編集
#### Windows
wslやvmでLinuxの環境を作成し、python3・makeコマンドが使えるようにしてください。  
リポジトリをクローンし、ルートで ```$ make install_dependence ```を実行後、 ``` $ mkdocs serve ``` で編集中の内容を即座に確認できます。

#### Mac/Linux
リポジトリをクローンし、ルートで ```$ make install_dependence ```を実行後、 ``` $ mkdocs serve ``` で編集中の内容を即座に確認できます。

### Tip
Markdownで
```
!!! Note
!!! Tip
```
などが利用できます。強調したいところを囲えるので便利です。


### ページのビルド
ファイルを編集してコミット(push)した段階でGithubActionsのworkflowが走りページをビルド・デプロイします。  
コミットidの横の 🟠 が　✅　になるとページのデプロイが完了したことを示します。  
デプロイには1-2分かかります。これはGithubActionsの設定で毎回vmのセットアップをしてしまっているからです。  
より良い方法があれば、書き換えてください。
