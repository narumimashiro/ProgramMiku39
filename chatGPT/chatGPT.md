# chatGPT概要

GPT(Generative Pre-trained Transformer)の略
大規模言語モデルLLMの一つ

人工知能研究所OpenAIが開発

Google検索との違いはキーワードを考える必要があるが、
ChatGPTはその考える工程すらやらなくてもよくなる

10の24乗のデータ量を超えたタイミングで急激に精度が良くなった

## **chatGPTの精度が高める方法**

人に聞くのと同じ

お互いを知らない関係で相談をすることを想定する

知らない人との会話で曖昧な質問をすると正確な返答がかえって来ない

なので、AIに大して前提条件をしっかり渡してあげることが大事

よりよい回答を得るために
1.役割を与える(職業を与えるイメージ)

あなたはプロのライターです
あなたは一流のデザイナーです
など

2.前提情報

やりたいことの背景を伝える
商品の特徴はなになにだ
まるまるを前提としています
など

3.制約条件
返答の表現方法を絞ること

専門用語を使わない
PREP法を使って
箇条書きで

など


明確化
この情報、この条件から返答をください

加工
表形式にしたり、チェックリスト
Markdownにするなど


テンプレート
```
あなたはプロの編集者です。
以下の制約条件と入力を元に、最高の要約を出力をしてください

# 制約条件
・文字数は300文字程度
・小学生にもわかりやすい
・重要なキーワードを取り残さない
・文章を簡潔に

# 入力
<聞きたいこと>
```

## **プロンプトを作成してもらう**

chatGPTに大して曖昧な情報しか与えない場合、大した返答は期待できない
かと言って、一発で最適な指示だしをすることも容易ではない、
そんなときにはプロンプト(指示文)すらChatGPTに作成してもらう方法を取ることができる

サンプル
```
あなたはChatGPTへの入力プロンプトを生成するプロンプトデザイナーです
私との会話を通して目的に会ったプロンプトをつくる手伝いをしてほしいです

# 目的

# 流れ
プロンプトを作るために必要な指示や情報があれば聞いてください
私が「プロンプトを作って」と言ったら、今までの会話を元にプロンプトを生成して出力してください
会話調でやりとりしてください

理解しましたか？問題なければ了解と、この実現に足りていない指示や情報があれば聞き返してください
```
