- [chatGPTをより効率よく使う方法](#chatGPTをより効率よく使う方法)
  - [変数を使ってみる](#変数を使ってみる)
  - [コマンド(関数)を使ってみる](#コマンド関数を使ってみる)
  - [繰り返しで品質をあげる](#繰り返しで品質をあげる)
  - [ゴールシークプロンプト](#ゴールシークプロンプト)
    - [chatGPTのプロンプト構成イメージ](#chatGPTのプロンプト構成イメージ)
      - [変数やコマンドなどが使えることを受けて(#TODO List)](#変数やコマンドなどが使えることを受けてTODO-List)

# chatGPTをより効率よく使う方法

## 変数を使ってみる

chatGPTは変数を用いて、プロンプトを作成することが可能です。

変数は`[変数名]:値`の形でチャット欄に書くだけです。

以下、変数を用いてプロンプトの例です

```text
[都道府県]:福岡県
[都市]:博多
[グルメ]:ラーメン

[都道府県]の[都市]周辺に旅行に行くので、[グルメ]が美味しいお店をいくつかピックアップしてほしい
```
## コマンド(関数)を使ってみる

コマンドを作成することも可能、chatGPTではコマンドとよく言われるが、我々が慣れ親しんだ名称で言うと関数のこと。

テンプレートは
```text
[コマンド名]
実行したい内容
スペース
```

以下、コマンドを用いてプロンプトの例です

```text
# 変数
[都道府県]:福岡県
[都市]:博多
[グルメ]:ラーメン

# コマンド
[SearchGourmet]
[都道府県]の[都市]周辺に旅行に行くので、[グルメ]が美味しいお店をいくつかピックアップしてほしい

[SearchGourmet]を実行
```

## 繰り返しで品質をあげる

以下のように開始地点を終了地点を指定してあげて、繰り返し実行を命じると繰り返した分だけ品質が上がった返答が期待できます

```text
下記の前提条件を元に、[開始]から[終了]の内容を3回繰り返して内容を改善してください

## 前提条件
[テーマ]:新入社員向けビジネス研修プログラム
[本文]:{本文}

## 出力
[テーマ]に沿って[本文]を作成してください

[開始]
[本文]の改善案を書き出してください
改善案を元に[本文]を再作成してください
[終了]
```

## ゴールシークプロンプト

先にゴール自分のやりたいことを設定して、どのようにしたらそれが達成できるかを手順を分解して探索していく方法のこと

### chatGPTのプロンプト構成イメージ

- コマンド1 : 必要な手順を分解する
- コマンド2 : 必要な変数を抽出し、ゴールを再定義する
- コマンド3 : ゴールを達成するためにコマンド1の手順を一つずつ実行

<Details><Summary>ゴールシークプロンプト例</Summary>

```text
[Goal]: 初音ミクで元気の出る曲の歌詞を考える

#######

[C1]
Goalを達成するために必要な手順をステップバイステップで実行できるように、
手順[P#]に分解してください。


# 出力
[P1]=
...
[P#]=
...
[P(END)]=

######

[C2]
[Goal]を必要条件として必ずインプットしてください
[Goal]を達成するために必要な変数を[Added Variable]とします


# 出力
[Added Variable]をリスト形式で書き出してください
[Goal]の定義を[Added Variable]を含めて再定義してください

[Goal] : {Goal}

######

[C3]
再定義された[Goal]を達成するために[P1]から[P#]を経て[P{End}]まで一つずつ実行してください

# 出力
[O1] = {Output[P1]}
....
[O#] = {Output[P#]}
....
[O{END}] = {Output[P{END}]}


Run [C1][C2][C3]
```

</Details><br>

<Details><Summary>chatGPTからの返答</Summary>

```text
[C1]
初音ミクで元気の出る曲の歌詞を考えるための手順をステップバイステップで分解します。

出力
[P1]= 曲のテーマやメッセージを決定する
[P2]= メロディやリズムを頭に描く
[P3]= 曲に合わせてコーラスやフックを考える
[P4]= ストーリーやシーンを元にサビやヴァースを考える
[P5]= 歌詞全体をリファインして、無駄な部分を削除・修正する
[P6]= 曲と歌詞のバランスを確認する
[P(END)]= 最終的な歌詞を完成させる

######

[C2]
[Goal]を達成するために必要な変数を定義します。

出力
[Added Variable]= 
テーマ
メロディ
リズム
コーラス
フック
ストーリー/シーン
サビ
ヴァース

[Goal] : 初音ミクで元気の出る曲の歌詞を、[テーマ]、[メロディ]、[リズム]、[コーラス]、[フック]、[ストーリー/シーン]、[サビ]、[ヴァース]を考慮して考える。

######

[C3]
再定義された[Goal]を達成するための手順を実行します。

出力
[O1] = {Output[P1]} : テーマは「希望と新しい始まり」にする
[O2] = {Output[P2]} : メロディはアップテンポで明るく、リズムはドラムとシンセを主体にする
[O3] = {Output[P3]} : コーラスは「希望の光が、新しい日を照らす」、フックは「輝く未来へ」を繰り返す
[O4] = {Output[P4]} : サビは「新しい日々、新しい夢、輝く未来へ」、ヴァースは「日常の中で見つけた小さな喜び、困難を乗り越えてきた経験」を元にする
[O5] = {Output[P5]} : 無駄な部分を削除し、歌詞の流れを自然にする
[O6] = {Output[P6]} : メロディやリズムと歌詞のバランスが良いか確認する
[O{END}] = {Output[P{END}]} : 歌詞を完成させ、初音ミクに合わせて最終調整する。
```

</Details>

#### 変数やコマンドなどが使えることを受けて(#TODO List)

chatGPTAPIとWebページの組み合わせで食べログのようなオリジナルサイトが作れるかも

- DBに検索データ残しておき、履歴機能を追加
- 身内だけアクセスできるようにして、検索結果などは共有で見れるようにしたら思い出にも良さそう
- AWSのSNSだったり、DiscordなどもAPIありそうなので、検索結果を簡単に身内に共有する機能もあったら良さそう
- ★レシピサイト作れそう！