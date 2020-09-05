# Qiita記事執筆用デモリポジトリ

https://qiita.com/gawgaw-2020/items/7d333248c7a2479aa4e4

---
title: Gitはじめましてから毎日GitHubに草を生やして継続してみた
tags: GitHub Git 初心者 VSCode
author: gawgaw-2020
slide: false
---
# Gitはじめましてから毎日GitHubに草を生やして継続中
はじめまして、がうがうです。

学習を始めるまでGit・GitHubに対して「よくわからない・怖い」と思っていた私ですが、
プログラミング・マークアップの勉強を始めて1週間経過しました。

GitHubへのプッシュも慣れ、楽しく草活できているそんな私の体験の覚え書きです。

いつも「新しいリポジトリ作る〜初回プッシュで草生やすまで」を忘れていた初心者の私が自分自身へ向けた記事です。

## この記事を読むと
「とりあえずGit・GitHub触ってみたい」「まずはGitHubに草生やしてみたい」という方は多少参考になるかもしれません。
GitHubの画面に緑の草を生やすことができます。（草活）
![スクリーンショット 2020-09-05 11.17.26.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/50996713-71ac-f3a0-9175-14aa5d239e8e.png)


### 対象
Git・GitHubを触ってみたいと思っている人

### 筆者のレベル感
同じくらいの方に参考になるかもしれません

- [x]  情報収集はじめて3ヶ月目（知人やSNSなど）
- [x]  コード書き始めて1週間経過
- [x]  Git / GitHubの違いを知らなかった

## 草の生やし方
そもそもGit・GitHubとは？というかたはこちら。
[Gitを使ったバージョン管理｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/intro/01/)

### Gitの準備
以下MacOS向けの記事になります。
Windowsの方はこちら
[【Windows】Gitの環境構築をしよう！](https://prog-8.com/docs/git-env-win)

#### ターミナルをつかう

Finderから、
アプリケーション＞ユーティリティ＞ターミナル.appを起動します。
よく使うので、すぐ使える場所に置いておくのがいいかもしれません。
![スクリーンショット 2020-09-05 12.54.03.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/a4dd2b78-cf1d-cdfb-46c8-4bc613b4768d.png)


#### ターミナルでバージョンを確認
Macの場合は初期インストールされているはずなので、ターミナルでバージョンを確認します。
※ コードの「\$」は打たなくて大丈夫です。「$」はプロンプトといい、コンピュータが命令を受け付けられる状態であることを示すものです。

```
$ git --version
```
結果以下のような表示が出ていればOKです。
出ない場合はダウンロードのウィンドウが表示されるので、確認後ダウンロードを行ってください。

```
$ git version 2.21.1 (Apple Git-122.3)
```

### Git上に自分のユーザー名とメールアドレスを登録

次にGitに自分の情報を登録します。


``name``と``nijipro@example.com``の部分に、自分の名前とメールアドレスを入れて、ターミナルで下記の2つのコマンドを打って下さい。

```
$ git config --global user.name "name"
$ git config --global user.email nijipro@example.com
```

### GitHubアカウントの作成
「GitHub」の無料アカウントを作成しましょう。

GitHubにアクセスします。
[GitHub](https://github.com/)

画面右側の、「ユーザーネーム」「メールアドレス」「パスワード」を入力して、「Sign up for GitHub」というボタンをクリックしてください。
![スクリーンショット 2020-09-05 10.52.55.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/7b858a4e-a88f-7906-541e-7496a8135e8b.png)

アンケートページに移りますが、答えなくても大丈夫です。私は英語は雰囲気で乗り切ります。
![スクリーンショット 2020-09-05 10.57.49.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/3ab97305-93ef-38ca-4f7f-e61187c40664.png)

登録したメールアドレスの認証も済ませれば、アカウントの作成は終了です。
![スクリーンショット 2020-09-05 10.59.29.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/e4a635b5-d663-4a1f-bf79-1f34af471a75.png)

こちらがホーム画面です。ぜひテンションが上がるお気に入りのアイコンを登録しましょう。
![スクリーンショット 2020-09-05 11.00.10.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/32369994-49a3-1405-f1ad-65af9a29db49.png)


### リポジトリの新規作成
GitHubアカウント上に新規リポジトリを作成します
リポジトリとはプロジェクトのようなものです。

画面右上アイコンの左の「+」をクリックし、「New repository」を選択します。
![スクリーンショット 2020-09-05 11.00.52.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/8ec55301-5713-ec05-dec8-2b9bfdff61df.png)


表示されたページの中央にある、「Repository name」という入力欄にリポジトリ名を入力します。ここでは``niji-project``とします。
「Public」「Private」を選択できますが、ここではPublicを選択します。Privateにすると非公開のリポジトリになります。また、下のチェックボックスにはチェックを入れなくて大丈夫です。

リポジトリ名を入力し、「Public」or「Private」を選択したら、「Create repository」をクリックしてください。

![スクリーンショット 2020-09-05 11.07.57.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/cb563b05-ae1a-01d0-6a5d-803746ff79e7.png)

これでリポジトリが完成したので、「…or create a new repository on the command line」の下にあるコードをまるっとコピーしておいてください。
![スクリーンショット 2020-09-05 11.13.59.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/951217c7-e8f4-86db-504b-0a4bb27c8571.png)


### 作業するフォルダを作成
デスクトップなどにフォルダを作成
ここではリポジトリ名と同じ``niji-project``とします。
![スクリーンショット 2020-09-05 11.30.56.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/fd61ab9a-53f5-400c-65d8-b85ba6ceaab2.png)



### VScodeで連携
VSCodeを起動して、先ほど作成した``niji-project``フォルダを開きます。
![スクリーンショット 2020-09-05 11.37.28.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/2b4fc7a1-aacb-372b-e65e-2af14fceae79.png)

VSCode上でターミナルを開きます。メニューバーの「ターミナル」→「新しいターミナル」を選択します。
![スクリーンショット 2020-09-05 11.38.37.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/2b17653a-47b5-8b99-0d9b-93a9f1cda8ae.png)

画面下部にターミナルが開くので、そこに先ほどコピーしたコードをそのまま貼り付けます。
![スクリーンショット 2020-09-05 11.41.57.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/ca24edb6-b0f6-3d3b-ac9f-ca16c49ec89d.png)

そのままEnterを押すと、コードが実行されます。
![スクリーンショット 2020-09-05 11.43.51.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/7efa2c96-0a21-a866-d758-153feec307a8.png)

このコマンドで「README」というファイル作成から、プロジェクトのローカルリポジトリが作成され、リモートリポジトリを関連付け、ローカルリポジトリの変更内容をリモートリポジトリに送信するところまでとりあえず進めることができます。（このあたりは触りながら覚えていければいいかなと思っています。）


### フォルダに変更を加えて、リモートリポジトリに反映させる
例として、新規ファイル作成します。ここでは``index.html``とします。
![スクリーンショット 2020-09-05 11.54.43.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/2eed6888-a205-c7eb-6ce7-6c7bcc3e5e58.png)

新規作成や変更をステージングします。変更を加えて保存すると、一番左の上から3つ目のアイコンにバッジがつくはずなのでそちらをクリックします。
変更があったファイルが並んでいるので、中央の「+」ボタンを押すと、ファイルが「ステージング」されます。
![スクリーンショット 2020-09-05 11.56.34.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/abf900e4-980f-e284-e96d-50be1cc49957.png)

こちらがステージングされた状態です。「変更を確定する前段階」といったイメージです。
![スクリーンショット 2020-09-05 11.57.36.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/b13957dd-8d78-8ba4-702a-aebded45fceb.png)

入力欄に変更内容のメッセージを入力します。
![スクリーンショット 2020-09-05 11.58.49.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/c78b51ee-e0a3-16cc-a267-6b97653bf6b1.png)

その後、メッセージ入力欄の上にあるチェックボタンをクリックします。
左のアイコンのバッジが無くなっていればOK。これで「コミット」された状態です。
![スクリーンショット 2020-09-05 11.59.27.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/5b04f2ce-034e-91d6-f548-031940ec129e.png)

最後に、変更内容を、GitHub上にアップロードします。先ほどのチェックボタンの右に「・・・」ボタンがあるので、「プル、プッシュ」→「プッシュ」をクリックします。これでGitHub上にアップロードされます。
![スクリーンショット 2020-09-05 12.00.16.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/a4073461-b299-db2c-ac09-465375e0fa6d.png)

GitHubのリポジトリを確認すると、ファイルが新しく追加されています。これを繰り返して、変更履歴を積み上げていきます。
![スクリーンショット 2020-09-05 12.18.27.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697564/f8a2f27b-ad13-ac48-5830-057e733219e2.png)


### マークダウン記法
現在私は、READMEに勉強したことをメモしているのですが、マークダウン記法の勉強になるのでおすすめです。
このQiitaもマークダウン記法で書いています。慣れるまで大変そうです。

## その他

### GitHubに上げちゃいけないコード
GitHubにアップロードしたコードは全世界に公開され、誰でも閲覧できるので注意が必要です。
* パスワード
* データベース接続のパスワード
* 機密情報

ファイルを削除して再アップロードしても、履歴から復元できてしまうので、履歴を消さないといけません。

### リポジトリをプライベートにしたいけど草は生やしたい
プライベートリポジトリにすると他のユーザーが訪問した際に緑が見えなくなります。プライベートリポジトリでも緑を披露したい方は設定の変更が必要です。
[プライベートリポジトリ で 草を 生やそう](https://qiita.com/miriwo/items/4e938b817a4d2425ef31)

### リポジトリを削除すると草は禿げる
私は2日目にして草が禿げてしまいました。
[リポジトリを削除するとGitHubの草は禿げる](https://mom0tomo.github.io/post/github_glass_become_bald/)

あと緑の色の濃さはコードの量だと思っていましたが、どうやら違うようです。
[Githubの草の色でひとの活動量を判断してはいけない理由](https://qiita.com/DQNEO/items/923d838d91f76dbeabd4)

## 感想
今回の記事の内容はGit・GitHubの機能の1％にも満たないと思いますが、毎日開いて「画面に慣れる」というのがとても重要だなと感じました。
また、毎日草活が継続するとモチベーションアップにも繋がるので、学習を始めた方は早めに使い始めるのがおすすめです。

ですが、1週間ほど草活して、草が生える達成感に浸るのもいいのですが早めに本格的な学習に移った方がいいなと感じています。
現在下記の教材で学習中ですが、バージョン管理のそもそもの考え方を丁寧に解説しているので理解しやすいです。（他にもおすすめ教材探し中です。）

[Git： もう怖くないGit！チーム開発で必要なGitを完全マスター](https://www.udemy.com/course/unscared_git/)

もしこちらの記事を読んで下さった方には、本格的なGit・GitHubの学習への足掛かりになれば幸いです。

## 参考

[Gitを使ったバージョン管理｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/intro/01/)
[【Windows】Gitの環境構築をしよう！](https://prog-8.com/docs/git-env-win)
[プライベートリポジトリ で 草を 生やそう](https://qiita.com/miriwo/items/4e938b817a4d2425ef31)
[リポジトリを削除するとGitHubの草は禿げる](https://mom0tomo.github.io/post/github_glass_become_bald/)
[Githubの草の色でひとの活動量を判断してはいけない理由](https://qiita.com/DQNEO/items/923d838d91f76dbeabd4)
[Git： もう怖くないGit！チーム開発で必要なGitを完全マスター](https://www.udemy.com/course/unscared_git/)

