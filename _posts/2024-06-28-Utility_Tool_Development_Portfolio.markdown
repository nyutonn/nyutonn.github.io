---
layout: post
title: 便利ツール開発
date: 2024-6-28 21:40:00 +0900


# subtitle: 趣味のゲーム開発の記録
thumbnail-img: /assets/img/excel.png
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
* 趣味の便利ツール開発の記録です
* ツールの概要，開発期間，使用言語，デモ動画をまとめています

<br>

## ExcelAttendanceToPDF
<img src="/assets/img/excel_button.png" width="700x400">

### 概要
* PDF自動生成ツール
* Excelマクロ，VBAを用いた
* ボタン一つで，全メンバーから出欠メンバーのみ別シートに抽出しつつ，表をPDF化する
* [GitHub](https://github.com/nyutonn/ExcelAttendanceToPDF)にてプログラムを公開しているものもあります


### フォルダの説明
* bas_files（VBA）フォルダにはVBAファイルが入っています
* demo_movieフォルダにはmacとwindowsの操作説明の動画が入っています
* excel_fileフォルダにはエクセルのファイルが入っています
* submission_docには，実際にPDF自動化で出力した書類が保存されています

### デモ動画
<ul class="horizontal-list">
    <li>Windows 事前準備
    <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/windows_事前準備.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>Mac 事前準備
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/mac_事前準備.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>Windows PDF自動出力手順
    <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/windows_PDF保存_簡易版.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>Mac PDF自動出力手順
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/mac_PDF保存_簡易版.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>Windows 体温手動入力手順
    <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/windows_PDF保存_体温手動版.mp4.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>Mac 体温手動入力手順
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/mac_PDF保存_体温手動版.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>

<br>

### 使用方法
<img src="/assets/img/excel_table.png" width="700x400">

* ##### 事前準備
1. 名前リストなどを外部からコピーしてC列の名前に貼り付ける
2. 左の表の学年，性別，学校名，電話番号を記入
3. 会員メンバーにはG列の会員Noを記入（非会員の場合は何も書き込まないこと）
<br><br>

* ##### PDF作成手順（簡易版）
1. レッスンに参加するメンバーの行に，D列（参加）のチェックマークを付ける
2. 上部にある「代表者氏名」と「レッスン日」を入力する
3. 上部にある赤色の「表作成＆PDF保存」ボタンを押す
4. 保存するフォルダを選択
<br><br>

* ##### PDF作成手順（体温手入力版）
1. レッスンに参加するメンバーの行に，D列（参加）のチェックマークを付ける
2. 上部にある「代表者氏名」と「レッスン日」を入力する
3. 上部にある緑色の「表を作成」ボタンを押す
4. 作成されたレッスン日の名前が付いたシートにて体温を記入する
5. 作成されたレッスン日の名前が付いたシートにて「現在の表をPDFに保存」ボタンを押す
6. 保存するフォルダを選択
<br><br>

* ##### その他の説明
  * これは出欠管理用のマクロファイルです．D列にチェックマークを付けたメンバーの表を作成し，PDFに保存します
  * 上部にある緑色の「表を作成」ボタンを押すと，参加メンバーの表を作成します
  * 上部にある赤色の「表作成＆PDF保存」ボタンを押すと，一度にPDF出力まで行います
  * 上部にある青色の「チェック全解除」ボタンを押すと，D列のチェックマークを全て外します
  * 表を作成した際に体温は35.8-36.5の間でランダムに決まります．変更する場合は値を上書きしてください．
  * 会員Noがある人は会員，ない人は非会員とみなされます．ただし「休」と書いてある場合には休会とみなし非会員扱いします
  * 上部にある白い「時を進める」を押すと学年が1増加し，「時を戻す」を押すと学年が1減少します．年度の変わり目にご使用ください．
<br><br>

* ##### 注意点
  * 表の列の追加や削除しないでください
  * 会員Noの列をG列から変更しないでください
  * 「表を作成」または「表作成＆PDF保存」ボタンを押すと同じ日付のシートがある場合には上書きされます
  * このシートの名前「メンバーリスト」は変更しないでください
  * 一般的にマクロ付きエクセルファイルは悪意を持ったユーザが作成するとウイルス感染することがあります．信頼できないマクロファイルは開かないようにしてください