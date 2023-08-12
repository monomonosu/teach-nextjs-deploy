
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

## vercelへのデプロイ
VercelへのデプロイはGUI上で行えます。  
まずは https://vercel.com/ へアクセスして画面右上の「sign up」から登録画面に飛び、「hobby」プランを選択。UserNameの入力もします。  
<img width="681" alt="スクリーンショット 2023-08-07 22 16 13" src="https://github.com/monomonosu/teach-nextjs-deploy/assets/77572073/4f88b80a-16ea-49f3-a98e-280870667ded">


GitHubログインで登録をしておきます。  
  
ダッシュボードに移動したら「Add Github Account」を選択し、Repositoryを選択できる状態にします。  

<img width="1229" alt="スクリーンショット 2023-08-11 20 38 16" src="https://github.com/monomonosu/teach-nextjs-deploy/assets/77572073/d76aa8af-0f06-4c31-9090-c185cee63860">

リポジトリが選択できる状態になったらデプロイしたいリポジトリの「Import」ボタンを押下します。  
<img width="753" alt="スクリーンショット 2023-08-12 18 09 23" src="https://github.com/monomonosu/teach-nextjs-deploy/assets/77572073/de4ff310-6ab0-4dbd-b492-a78432e7c7aa">
  
プロジェクト名を入力し、「Deploy」を選択。（その他設定が必要な場合は設定。）  
<img width="860" alt="スクリーンショット 2023-08-12 18 09 57" src="https://github.com/monomonosu/teach-nextjs-deploy/assets/77572073/9799c3c2-7e22-4f0b-9e59-6da3039732e3">
  
下記のような画面が出たらデプロイ完了です。  
アプリのプレビュー画面を押下するとデプロイしたURLに遷移する事ができます。  
<img width="1300" alt="スクリーンショット 2023-08-12 18 12 32" src="https://github.com/monomonosu/teach-nextjs-deploy/assets/77572073/dbc6fd92-3029-4642-921b-21fbce896943">
  
これ以降はリポジトリに差分をPushする度に変更が反映されるはずです。
  
下記がこのリポジトリを実際にデプロイしたものになります。  
URL:https://teach-nextjs-deploy.vercel.app/

