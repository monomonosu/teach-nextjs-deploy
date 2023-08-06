
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

## next.jsのビルド
next.jsセットアップ直後は`npm install`が必要みたいなのでコマンドの実行をお願いします。  

next.jsが正常にセットアップされているか確認のため、下記を実行  
`npm run build`  
`npm run start`  

こんな感じの画面が表示されればOKです。  
<img width="1719" alt="スクリーンショット 2023-08-06 16 34 55" src="https://github.com/monomonosu/teach-nextjs-deploy/assets/77572073/f5c2d309-e1f0-43f8-9447-e60bfd60376a">
  
