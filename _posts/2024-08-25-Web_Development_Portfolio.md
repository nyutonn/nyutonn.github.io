---
layout: post
title: Web開発ポートフォリオ
date: 2024-08-01 13:00:00 +0900


# subtitle: 趣味のゲーム開発の記録
thumbnail-img: /assets/img/kag_サムネ_RAG.png
# cover-img: /assets/img/milk.jpeg
# gh-repo: daattali/beautiful-jekyll
# gh-badge: [star, fork, follow]
# tags: [test]
comments: true
# author: Nakano Yuto
---

<!-- 写真や動画で箇条書きの点を表示させないためのクラス -->
<!-- 使用するところの先頭で <ul class="no-bullet"><li> を差し込む-->
<style>
  .no-bullet {
    list-style-type: none;
    padding: 0;
  }
  .no-bullet li {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
  }
  .no-bullet video, .no-bullet img {
    margin-right: 10px;
  }
</style>

<!-- 箇条書きを横に表示するクラス -->
<!-- 使用する先頭に <ul class="horizontal-list"><li> -->
<style>
  .horizontal-list {
    display: flex;
    padding: 0;
    list-style-type: none;
  }
  .horizontal-list li {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-right: 20px;
  }
  .horizontal-list video, .horizontal-list img {
    margin-bottom: 10px;
  }
</style>

## 概要
* インターンシップでチーム開発したWebアプリケーションの作品集です
* Webアプリケーションの概要，開発期間，使用言語・ツール，デモ動画をまとめています

<br>


## 目次
- [RAGを用いた社内情報チャットボット](#ragを用いた社内情報チャットボット)
- [記事推薦と新聞⾵ UI を⽤いたマイ新聞サービス](#記事推薦と新聞-ui-をいたマイ新聞サービス)

<br>

## RAGを用いた社内情報チャットボット
<img src="/assets/img/kag_サムネ_RAG.png" width="800x400">

##### 概要
* RAGを用いたKDDIアジャイル開発センター株式会社（以下KAG）の社内情報チャットボットとカジュアル面談ページ作成
  * 目的: 特定の大学生をペルソナとして，就活に割く時間がないという課題を解決する
  * 解決方法: 効率よくKAGの情報を就活生に伝える
  * 実装1: 対話形式で情報収集を行うための，RAGによるKAG特化チャットボット開発
  * 実装2: 従来よりもカジュアル面談にアクセスしやすくするための，新ページ作成
* KAGのアジャイル開発体験インターンシップにて，4人でチーム開発を行い，私個人はRAGの実装を担当
  * [インターンシップページ](https://kddi-agile.com/news/20240514-01)

##### RAGの実装
ユーザの入力文に関連するKAGの情報を検索して応答生成 ([参考ページ](https://qiita.com/minorun365/items/24dfb0ea3afde6ed0a56))

* KAGの情報をPDFに保存して簡易的なデータベースを作成
  * 必要な情報が含まれているページを1つのPDFに連結
    * 今回はデモ用に50MB程度の小規模なデータを使用
  * S3バケットにPDFをアップロード
  * ナレッジベースにてS3を参照
* 言語生成モデルとデータベースを同期
  * Amazon Bedrock の Claude 3.5 Sonnet とナレッジベースを同期
  * TypeScript上でAPIを呼び出す


##### 開発期間
* 2024.8.22-2024.8.23
* 2 日

##### 使用言語・ツール
* 使用言語: TypeScript
* インフラ: AWS (Amplify, S3バケット, ナレッジベース, Amazon Bedrock)
* 言語モデル: Claude 3.5 Sonnet
* 開発フレームワーク: デザイン思考 (ペルソナの課題解決をするストーリーボード作成), アジャイル開発 (スクラム, KDGポーカーを用いたコスト見積もり, Fun/Done/Learnを用いた振り返り)
* プラットフォーム: GitHub
* OS: macOS
* 開発環境: Coder, VS Code

上記の全ての技術スタックは私の担当範囲であるバックエンドの実装で用いたものであり，チームのペアが実装したフロントエンドに用いた技術スタックは含まれていません

<br>

##### デモ動画
* RAGを用いたチャット機能
    <ul class="no-bullet"><li>
    <video width="800" controls>
    <source src="/assets/movie/kag_デモ動画_RAG.mp4" type="video/mp4">
    </video></li></ul>
* カジュアル面談ページ
    <ul class="no-bullet"><li>
    <video width="800" controls>
    <source src="/assets/movie/kag_デモ動画_カジュアル面談.mp4" type="video/mp4">
    </video></li></ul>

<br><br>



## 記事推薦と新聞⾵ UI を⽤いたマイ新聞サービス
<img src="/assets/img/nikkei.jpg" width="600x300">

※ 著作権の関係で上記の画像はフリー素材です

##### 概要
* 個⼈の興味に合わせた記事推薦と新聞⾵ UI を⽤いたマイ新聞サービス
* 株式会社日本経済新聞社にて，ハッカソン形式の１週間の短期インターンシップにて開発
  * [インターンシップページ](https://hack.nikkei.com/internJobs/2024_summer/)
* 二人一組のチームで開発を行い，私は記事推薦アルゴリズムを実装するバックエンド側のAPI構築を担当

##### 推薦アルゴリズムとリランキング方法
* ユーザの好みの把握: 特定日 (2024/8/15) の日経電子版へのアクセス数トップ100人の閲覧履歴を収集して，好みのジャンル・業界・トピック・キーワードを集計して分析
* 一面の記事選択: 注目度の高い記事を推薦するために，ユーザの好みのジャンルについてページビュー数が多い記事を選択
* 二面以降の記事選択: ユーザの好みを反映させるために，記事の注目度だけでなく，ユーザの関心度や記事の新鮮度を考慮した重み付けスコアが高い記事を選択
<embed src="{{ '/assets/pdf/nikkei_backend.pdf' | relative_url }}" type="application/pdf" width="100%" height="600px" />

##### 開発期間
* 2024.8.12-2024.8.16
* 5 日

##### 使用言語・ツール
* 使用言語: Python
* 使用ライブラリ: 日経の記事データを取得する API，Flask
* データベース: BigQuery
* プラットフォーム: GitHub
  * Issuesを用いてタスク管理
  * プルリクエストを用いてコードレビュー
* OS: macOS
* エディター: VS Code

上記の全ての技術スタックは私の担当範囲であるバックエンドの実装で用いたものであり，チームのペアが実装したフロントエンドに用いた技術スタックは含まれていません