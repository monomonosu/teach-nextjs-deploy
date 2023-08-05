
next.jsのVercelへのデプロイ方法を記載しておきます。
もし教材で使用する場合はこちらのReadmeの手順に沿って頂ければ問題ないかと思います。

## nodeのインストール

もし対象となるPCにnodeがインストールされていなければnodeのインストールをする所から。
`https://nodejs.org/ja` でnodeをインストールできる。

## next.jsセットアップ

`npx create-next-app <app名>`
app名とgithubのリポジトリ名は合わせておいた方が良いかもです。

## git リポジトリ作成

git hub へのリポジトリを作成する。next.jsのセットアップ時に使用したapp名でリポジトリ名を作成します。

## git へのファーストコミット

作成されたappのディレクトリに移動します。
このappディレクトリにはすでに.gitが作成されているので`git init`等はしなくてOKです。
  
必要であれば下記を実行  
`git config --local user.name <userName>`
`git config --local user.email <userEmail>`
  
remote設定  
`git remote set-url origin https://<userName>:<token>@github.com/<userName>/<repositoryName>.git`
  
`git push origin main`
  
これでpushできるかと思います。