# サービス概要

個人開発に関する技術記事を

- 探しやすく
- まとめて管理しやすく

するための技術記事データベースです。

# メインのターゲットユーザー

- 個人開発に興味のあるエンジニア
- 未経験からのエンジニア転職を目指しているが、PF 作りに困っている人

# ユーザーが抱える課題

1. 個人開発で参考になる資料や記事は各種技術サイトや Web 上にたくさん存在しているが、それらをまとめた技術サイトは存在していないため、もし仮にユーザーがブックマークし忘れてしまった場合、探す手段がなくなってしまう。
   <br>

2. 技術サイトに投稿されている記事（Qiita・Zenn など）の場合、各サイトごとに保存機能も存在しているがバラバラに保存してしまうと、あとで見返したい時に不都合が生じる。
   （どのサイトのものだったのかわからなくなる...みたいなケース）

# 解決方法

個人開発に役立つ記事や資料を一元化した「データベース」を作成することで、保存し忘れやバラバラに管理することで生じる不都合を一気に解消する

（活用例）

- 保存し忘れどんな記事だったか忘れた場合は検索すればすぐに探し出せる
- 各種技術サイトでバラバラに保存していたものをまとめて管理することで見返す際にどの技術サイトのものだったか悩まなくて済む

# 実装予定の機能

以下、検索目的や保存目的の資料を「記事」と呼ぶ

## 一般ユーザー

- **<code>トップページに訪れたユーザーがカテゴリに紐づいた記事一覧画面に遷移できる</code>**
  - ユーザーがトップページの人気カテゴリを閲覧できる
    - ユーザーがトップページの人気カテゴリからカテゴリを直接クリックすることで、そのカテゴリに紐づいた記事一覧画面に遷移できる
  - ユーザーがトップページからすべてのカテゴリ画面に遷移できる
    - ユーザーがすべてのカテゴリ画面から調べたいカテゴリを検索することができる
      - 検索後、カテゴリを直接クリックすることでカテゴリに紐づいた記事一覧画面に遷移できる
    - ユーザーがすべてのカテゴリ画面からカテゴリを直接クリックすることで、そのカテゴリに紐づいた記事一覧画面に遷移できる
    - ユーザーがすべてのカテゴリ画面から人気のカテゴリを閲覧できる
      - 人気カテゴリのカテゴリをクリックすることで、そのカテゴリ紐づいた記事一覧画面に遷移できる
        <br>
- **<code>トップページに訪れたユーザーが記事を検索できる</code>**
  - ユーザーがトップページの急上昇中の記事を閲覧できる
    - ユーザーがトップページの急上昇中の記事から記事をクリックすることで、記事詳細画面に遷移できる
      - ユーザーが記事詳細画面から参照元の記事にアクセスできる
  - ユーザーがトップページからすべての記事画面にアクセスできる
    - ユーザーがすべての記事画面から直接記事をクリックすることで記事詳細画面に遷移できる
      - ユーザーが記事詳細画面から参照元の記事にアクセスできる
    - ユーザーがすべての記事画面から調べたい記事をタイトル検索できる
      - 検索後に記事をクリックすることで記事詳細画面に遷移できる
        - ユーザーが記事詳細画面から参照元の記事にアクセスできる
    - ユーザーが記事一覧画面上で「すべて」「急上昇中」「人気記事」タブを押すことで一覧画面の切り替えができる
      - 切り替わった画面上から記事を直接クリックすることで記事詳細画面に遷移できる
        - ユーザーが記事詳細画面から参照元の記事にアクセスできる
      - 切り替わった画面からもタイトル検索が可能
        - 検索後に記事をクリックすることで記事詳細画面に遷移できる
          - ユーザーが記事詳細画面から参照元の記事にアクセスできる
  - ユーザーがトップページから各カテゴリに紐づいた記事一覧に遷移できる
    - ユーザーが直接記事をクリックすることで記事詳細画面に遷移できる
      - ユーザーが記事詳細画面から参照元の記事にアクセスできる
    - ユーザーが調べたい記事をタイトル検索できる
      - 検索後に記事をクリックすることで記事詳細画面に遷移できる
        - ユーザーが記事詳細画面から参照元の記事にアクセスできる
    - 「すべて」「急上昇中」「人気記事」タブで一覧画面の切り替えができる
      - 切り替わった画面上から記事を直接クリックすることで記事詳細画面に遷移できる
        - ユーザーが記事詳細画面から参照元の記事にアクセスできる
      - 切り替わった画面からもタイトル検索が可能
        - 検索後に記事をクリックすることで記事詳細画面に遷移できる
          - ユーザーが記事詳細画面から参照元の記事にアクセスできる

<br>

## ログインユーザー

以下一般ユーザーが使用可能な機能はすべて使用可能の前提のもと記述する

- <code>**ユーザーがトップページ上の急上昇中の記事一覧上の各記事のいいね・ストックボタンを押下することができる**</code>
- <code>**ユーザーがカテゴリに紐づく記事一覧画面上の各記事のいいね・ストックボタンを押下することができる**</code>
- <code>**ユーザーがすべての記事画面から各記事のいいね・ストックボタンを押下することができる**</code>
- <code>**ユーザーがヘッダーのアバター画像をクリックするとマイページへ遷移できる**</code>
  - マイページ上でいいね・ブックマーク・コメントした記事の一覧を見ることができる
  - マイページ上の「いいね」「ブックマーク」「コメント」タブ押下で一覧画面の切り替えができる
  - マイページ上のプロフィール編集ボタンからプロフィール編集ページへ遷移できる
    - プロフィール編集ページで「アバター画像」「ニックネーム」「自己紹介」「GitHub ユーザー名」「Twitter ユーザー名」を更新することができる

## 管理ユーザー

- ログインユーザーの検索、一覧、詳細、編集
- カテゴリの一覧、詳細、作成、詳細、編集、削除
- 記事の一覧、詳細、作成、編集、削除
- 管理ユーザーの一覧、詳細、作成、編集、削除

# なぜこのサービスを作りたいのか？

自分が以前個人開発をしようとして技術記事や参考資料を調べていた際に、ブックマークのし忘れや各技術サイトごとにバラバラに保存してしまっていたため、あとで見返しそうと思ったときに非常に不便だった。

そのときに、個人開発に関する資料や技術記事だけをまとめたサイトがあったら便利だなぁと思い、開発するに至りました

# スケジュール

企画〜技術調査：12/3
README〜ER 図作成：12/3
メイン機能実装：12/3 - 1/10
β 版を RUNTEQ 内リリース（MVP）：1/10 〆切
本番リリース：2 月中旬
