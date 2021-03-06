# 話題に基づく語義曖昧性解消評価セット

## 内容

日本語の文について曖昧性を持つ単語に対して【話題】を付与したデータセットです。
例えば「ドライバー」という単語は「ゴルフのクラブ」「運転手」「ねじ回し」等、複数の意味を持っています。
これらに対して「ドライバーは安全運転をしなければならない」といった文中のドライバーに対して話題に基づくカテゴリ「自動車」を付与したものがこのデータセットとなります。
話題に基づくカテゴリは「[D11:話題分類単語辞書](http://www.jnlp.org/SNOW/D11)」に基づいたものを使用しています。
付与されるカテゴリは我々が独自に定義したものになっています。
話題辞書と組み合わせることで、語義に強く共起する単語群を容易に取得することが可能です。
データの抽出方法の関係上カテゴリに属さない文も含まれると考え、「その他」カテゴリを設けています。

## 既存の語義曖昧性解消タスクとの比較

既存の語義曖昧性解消データセットに比べて非常に粗い粒度のものとなっています。
日本語の語義曖昧性解消では岩波国語辞典の語義をベースにしたSemEval-2010 Task: Japanese WSD[1]が有名ですが、
それらに対して我々が公開するデータセットは粒度が話題単位であるため粗く、文脈が大きく異なるため比較的簡単であると想定されます。

## データセットに関して

データセットの作成方法については下記の関連文献[2]をご覧ください。
クラウドソーシングに基づき作成されたデータセットになっているため誤りなどが多く存在している場合があります。
GitHubにて同様のデータを公開しているので、もし使用に際して間違いなどを見つけた場合はPullRequestを投げてもらえると非常にありがたいです。

## データの内容

以下の例のようにデータが配列されています。

category | target_word | sentence
------------ | ------------- | ------------ 
自動車 | ドライブ | 週末はドライブには行けず、ひたすら寝てばかりいた…
卓球 | ドライブ | スピードドライブを打つには、ラケットの振りを上下ではなく…


* category : 付与された話題辞書のカテゴリ
* target_word : カテゴリ付与の対象単語
* sentence : 対象の文

## ライセンス, 論文, その他

以下をご参照ください。
[http://www.jnlp.org/SNOW/E19](http://www.jnlp.org/SNOW/E19)

## 参考文献

1. Okumura, M., Shirai, K., Komiya, K., Yokono, H.: SemEval-2010 task: Japanese WSD. In: Proceedings of the 5th International Workshop on Semantic Evaluation (Semeval 2010), Uppsala, Sweden, pp. 69–74 (2010)
2. 桾澤 優希, 山本 和英. 話題に基づく語義曖昧性解消. 言語処理学会第24回年次大会, pp.248-251 (2018.3)
