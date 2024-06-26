# ペアプログラミングとVSCode LiveShareについて

  - [1. ペアプログラミングのベストプラクティス](#1-ペアプログラミングのベストプラクティス)
    - [1.1 ペアプログラミングとは](#11-ペアプログラミングとは)
    - [1.2 ペアプロの原則](#12-ペアプロの原則)
    - [1.3 ペアプロのメリットデメリット](#13-ペアプロのメリットデメリット)
  - [2. LiveShareの導入](#2-liveshareの導入)
    - [2.1 LiveShareとは](#21-liveshareとは)
    - [2.2 インストール方法](#22-インストール方法)
    - [2.3 初期設定と認証プロセス](#23-初期設定と認証プロセス)
  - [3. LiveShareを用いたコード共有](#3-liveshareを用いたコード共有)
    - [3.1 セッションの開始方法](#31-セッションの開始方法)
    - [3.2 セッションの参加方法](#32-セッションの参加方法)
    - [3.3 機能の使い方](#33-機能の使い方)
  - [4. 注意点とトラブルシューティング](#4-注意点とトラブルシューティング)
  - [5. 参考ページ](#5-参考ページ)

## 1. ペアプログラミングのベストプラクティス

### 1.1 ペアプログラミングとは

ソフトウェア開発の手法の一つで、2人の開発者が1台のコンピュータを共用してプログラミング作業を行う方法です。

このアプローチは、アジャイル開発プロセスの一環としてよく用いられます。

### 1.2 ペアプロの原則

ペアプロには主に「`ドライバー`」と「`ナビゲーター`」という2つの役割があります

- ドライバー

コードの入力を担当し、コーディングの「運転手」の役割を果たします。ドライバーは、ナビゲーターか

- ナビゲーター

全体の方向性を監視し、コードの構造、将来の問題点、リファクタリングの機会などについて考える役割を持ちます。

ナビゲーターは、ドライバーがコーディングに集中できるように、より大きな視点からプロジェクトを見守ります。

---

またペアプロの基本的な原則として「`相互学習`」、「`コミュニケーション`」、「`相互尊重`」、「`継続的なフィードバック`」、「`ロールの交代`」の5つがあげられます

- 相互学習

経験や知識の共有を通じて相互に学び合う、知識のギャップを埋める絶好の機会です。

- コミュニケーション

ペアの両者が考えていることを声に出して共有することで、誤解を避け、より効率的に作業を進めることができます

- 相互尊重

異なるバックグラウンドやスキルレベルから来る新しいアイデアを受け入れることで、より革新的な解決策にたどり着くことができます

- 継続的なフィードバック

コードを書いた直後にフィードバックを得ることができます。これにより、問題を早期に特定し、修正することができます

- ロールの交代

ドライバーとナビゲーターの役割は、定期的に交代することが推奨されます。

これにより、ペアの両者がプロジェクトの異なる側面を理解し、スキルを均等に向上させることができます


### 1.3 ペアプロのメリットデメリット

メリットとしては以下が一般的にあげられます

1. コードの品質向上

2人の開発者がコードをレビューしながら進めるため、バグや設計の問題を早期に発見しやすくなります。

2. 知識の共有

開発者間で知識やスキルが共有されるため、チーム全体の技術力の向上につながります。

3. コミュニケーションの促進

継続的なコミュニケーションが求められるため、チームメンバー間の相互理解が深まります。

デメリットは以下が一般的にあげられます

1. リソースの増加

2人の開発者が同じタスクに取り組むため、一見すると労力の二重投資のように見えることがあり、コスト効率が懸念される場合があります。

2. 個人の作業スタイルの違い

作業者のスタイルやペースが異なるため、この違いがストレスや不満を引き起こす可能性があります

3. プライバシーの欠如

他人に観察されながらの作業となるため、ストレスの原因となる可能性がある

## 2. LiveShareの導入

### 2.1 LiveShareとは

Visual Studio Code (VSCode) の LiveShare は、開発者がコードをリアルタイムで共有し、リモートで協力して作業を進めることができる強力な拡張機能です。

このツールは、複数の開発者が同じコードベース上で同時に作業し、編集内容を即座に互いに反映させることを可能にします。

LiveShare は、VSCode の環境内で直接動作し、追加のソフトウェアや複雑な設定を必要としません。

### 2.2 インストール方法

VSCodeの拡張機能ビューから「LiveShare」と検索してインストール

### 2.3 初期設定と認証プロセス

LiveShareを利用するためには`Microsoft`か`Github`の認証が必要です。

LiveShareのアイコンからセッションの開始をしようとするとMicrosoftかGithubでのサインインが要求されるので、指示に従いサインインをするだけで初期設定は完了しLiveShareが利用可能になります。

## 3. LiveShareを用いたコード共有

### 3.1 セッションの開始方法

1. LiveShareのアイコンをクリックすると「Share(Read/Write)」、「Share(Read-Only)」、「Join」の3つのボタンが出てくるので、「`Share(Read/Write)`」を選択

2. ボタンが表示されていたエリアがSessionDetailsに代わり、ParticipantsやShared Terminalsタブが出てくる(※初期設定がまだの方はここでサインインが求められる)

3. Participantsの中にある「`Invite participants`」をクリック。もしくはSessionDetailsとかいてあるエリアの右端にある「`Copy Collaboration Link`」をクリックして、招待URLを取得し、参加者に共有する。


### 3.2 セッションの参加方法

1. 共有してもらった招待URLをクリック。もしくはLiveShareのJoinボタンから招待URLを入力して決定

2. サインインして参加か匿名での参加が可能だが、サインインして参加が推奨

### 3.3 機能の使い方

- リアルタイムのチャットと音声通話機能

コード共有だけでなく、チャットや通話機能も備わっている

- サーバーのポート共有

ローカルサーバーのポートをセッション参加者と共有することが可能。

ホストの方が`npm run dev`でアプリ起動したものをLiveShareを介して共有し実際に確認することができる

```text
SessionDetailsの項目にある、Shared Serversに`http://localhost:3000/`を記入すると参加者も開いているソースコードでのWebページを見ることができる
```

- 参加者を強制的に同じファイルを見るようにする

VSCodeの右上にあるメガホンマーク「Focus Participants」ボタンを押下することで参加者に自分の見ているファイルの表示を強制させることが可能

〇〇ファイルの...などと通達する必要なく同じファイルの参照が可能

- 参加者の動作を追尾することも可能

VSCodeの右上にあるピン止めマーク「Follow Participants」ボタンを押下すると、参加者の動作をそのままトレースして追っていくことが可能である

<Details><Summary>実際に使ってみたうえでの小ネタメモ</Summary>

- 今自分が見ている画面を相手は見ているわけではない

あくまでフォルダを共有してリアルタイムで更新できるものであり、画面共有というわけではない

ですので、AさんがHoge.tsxファイルを開いて作業中にBさんがFuga.tsxファイルを開いてもAさんのVSCode上でFuga.tsxファイルに切り替わることなく、Bさんは作業ができる

- 同じファイルを見ている場合はカーソル位置などは把握できる

同じファイルであれば、カーソル位置はVSCode画面上に表示されるため、画面共有のような形で作業は可能

</Details>

## 4. 注意点とトラブルシューティング

- プライバシーとセキュリティ

LiveShare開始したフォルダのすべてが共有されるため、信頼関係が大事である

ファイルの修正やファイルの削除なども行えてしまう。また機密情報などが誤って含まれていた場合情報漏洩につながります

対策として「.vsliveshare」設定ファイルを使用して、除外するファイルやディレクトリを設定することが可能

## 5. 参考ページ

[LiveShare公式ページ](https://learn.microsoft.com/en-us/visualstudio/liveshare/use/install-live-share-visual-studio-code#join-a-collaboration-session)

[Learn LiveShare](https://learn.microsoft.com/ja-jp/visualstudio/liveshare/use/install-live-share-visual-studio-code)