## 参考記事
- HugoのWindowsでの使い方はこれ！[Hugo を試す（Windows）](https://www.imuza.com/entry/2018/02/09/164628)
- Amplifyはこれ！[AWS Amplifyコンソールを使ってHugoベースの静的サイトを構築](https://dev.classmethod.jp/cloud/aws/hugo-hosted-on-aws-amplify-console/)

## 実行コマンドまとめ
```
# Windowsで実行

md C:\hugo
cd C:\hugo
md sites bin

# hugo.exe をダウンロードしてきて、bin/配下に入れる。

# C:\hugo\bin にパスを通す

hugo new site hugotest
cd hugotest
git init
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke # ここが参考サイトと違うコマンドを打っているところで肝になる。
echo theme = "ananke" >> config.toml
hugo new posts/my-first-post.md
hugo server -D

# http://localhost:1313/とかでWebページが見れるようになっている。

# GitHubで新たに「hugotest」というリポジトリを作成

git remote add origin git@github.com:codesmith/hugotest.git
git add .   # C:\hugo\sites\hugotest\直下で実行
git commit -m "seikou"

# 後はAmplifyで新規アプリを作成すれば良いだけ。

```
