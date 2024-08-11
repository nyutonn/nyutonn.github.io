---
layout: post
title: ゲーム開発ポートフォリオ
date: 2023-12-21 13:00:00 +0900


# subtitle: 趣味のゲーム開発の記録
thumbnail-img: /assets/img/tetrimino.jpg
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
* 趣味のゲーム開発の記録です
* ゲームの概要，開発期間，使用言語・ツール，プレイ動画をまとめています
* [GitHub](https://github.com/nyutonn/GameDevelopment/tree/main)にてプログラムを公開しています

<br>

## 目次
1. [CUIドラクエ風RPG](#cuiドラクエ風rpg)
2. [GUIポケモン名前当てクイズ](#イラスト名前当てクイズ)
3. [CUIテトリス](#guiテトリス)
4. [LEDリズム天国](#ledリズム天国)
5. [ネットワーク対戦型オセロゲーム](#ネットワーク対戦型オセロゲーム)
6. [Unity](#unity)

## CUIドラクエ風RPG
<img src="/assets/img/rpg_ドラクエ風RPGサムネイル.png" width="800x400">

##### 概要
* 短期間でC++を用いて作成したCUIドラクエ風RPG
* １週間のC++新人研修体験短期インターンシップの最終提出課題として作成
* メモリアロケーター（Pool Allocator）を用いたメモリ管理
* ステートマシンを用いたゲーム状態の管理
  * 状態遷移の詳細は [GitHub 上の project_drawings フォルダ内のPDF](https://github.com/nyutonn/GameDevelopment/blob/main/2024_8_CUI_DORAGON_QUEST_ike_RPG/project_drawings/ドラクエ風RPG操作説明.pdf)に記載
* ゲームプログラムは[GitHub](https://github.com/nyutonn/GameDevelopment/blob/main/2024_8_CUI_DORAGON_QUEST_ike_RPG/game_main/CUIドラクエ風RPG_mac/run.cpp)にて公開

##### 開発期間
* 2024.8.8-2024.8.9
* 2 日

##### 使用言語・ツール
* 使用言語: C++
* OS: macOS・WindowsOS
* エディター: VS Code・Visual Studio 2022

##### プレイ動画
* ゲームオーバー
    <ul class="no-bullet"><li>
    <video width="800" controls>
    <source src="/assets/movie/rpg_ゲームオーバー.mp4" type="video/mp4">
    </video></li></ul>
* ゲームクリア
    <ul class="no-bullet"><li>
    <video width="800" controls>
    <source src="/assets/movie/rpg_ゲームクリア.mp4" type="video/mp4">
    </video></li></ul>

<br><br>


## GUIポケモン名前当てクイズ
<!-- 著作権 -->
<!-- イラストや使えばいいのでは？ -->
<!-- ゲーム・アプリ・ソフトウェア・プログラムへの利用でないこと -->

<img src="/assets/img/pokemon_ニャオハ.jpg" width="400x400">

##### 概要
* GUI ポケモン名前当てクイズゲーム
* 当時SNSで流行していた[ポケモン全部言えるかな？](https://all-pokemon-ierukana.com/)に感銘を受け，ライトユーザー向けのより簡単なクイズを作成
* イラストの名前を当てるクイズ
* ヒントボタンを押すと頭文字と文字数がわかるようになる
* 著作権の関係で友人に書いて頂いたイラストを用いたクイズ動画となっている

##### 開発期間
* 2023.4-2023.5
* 約1ヶ月

##### 使用言語・ツール
* 使用言語: Python
* ライブラリ: tkinter (GUI)
* OS: macOS
* エディター: VS Code

##### プレイ動画
* クイズ動画
    <ul class="no-bullet"><li>
    <video width="600" controls>
    <source src="/assets/movie/pokemon_play.mp4" type="video/mp4">
    </video></li></ul>


<br><br>


## GUIテトリス

<img src="/assets/img/tetris_タイトル画面.png" width="400x400">

##### 概要
* 既存のテトリスに追加要素を加えたゲーム
* タイトル画面とテトリミノのグラフィックに拘り
    <ul class="no-bullet"><li>
    <img src="/assets/img/tetrimino.jpg" width="200x200">
    </li></ul>
* 初めてのゲーム開発経験
* ゲームプログラムは[GitHub](https://github.com/nyutonn/GameDevelopment/blob/main/2021_1_Tetris/game_main/tetris_run.hs)にて公開

##### 開発期間
* 2020.10-2020.12
* 約3ヶ月

##### 使用言語・ツール
* 言語: Haskell
* OS: Ubuntu on Windows PC
* エディター: Emacs

##### プレイ動画
<ul class="horizontal-list">
    <li>フリーモード
    <ul class="no-bullet"><li>
        <video width="300" controls>
        <source src="/assets/movie/tetris0_free_game.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>オートドロップモード
        <ul class="no-bullet"><li>
        <video width="300" controls>
        <source src="/assets/movie/tetris1_auto_dtop.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>テトリミノ選択モード
        <ul class="no-bullet"><li>
        <video width="300" controls>
        <source src="/assets/movie/tetris2_select_tetrimino.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>10000スコアモード
        <ul class="no-bullet"><li>
        <video width="300" controls style="margin-right: 10px;">
        <source src="/assets/movie/tetris3_10000score_challenge.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>スペシャルモード
        <ul class="no-bullet"><li>
        <video width="300" controls>
        <source src="/assets/movie/tetris4_special_mode.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>


<br><br>


## LEDリズム天国
<img src="/assets/img/rhythm0_ポスター_オリジナルバリバリ三人衆.png" width="600x600">

##### 概要
* ラズベリーパイを用いて開発したリズム天国風リズムゲーム
* 初代リズム天国GBA「パチパチ三人衆」「バリバリ三人衆」の音楽にノッて，リズムに合わせてボタンを押す
* 2つのLEDが順に光るので，リズムに合わせて3つめのLEDを点灯させる
* 押したタイミングに合わせて4つめのLEDの色が変化する
* 曲が終わった際に得点を集計し，7セグメントLEDでレベル 0 ~ 9 で表示される
* ゲームプログラムは[GitHub](https://github.com/nyutonn/GameDevelopment/tree/main/2023_1_Rhythm_Heaven_LED/game_main)にて公開

##### 開発期間
* 2022.12-2023.1
* 約1ヶ月

##### 使用言語・ツール
* ハードウェア: ラズベリーパイ (Raspberry Pi)
    <ul class="no-bullet"><li>
    <img src="/assets/img/rhythm1_プレイ画像1.jpg" width="300x300">
    </li></ul>
* 言語: Python
* OS: Windows OS
* ターミナル: Windows Terminal
* エディター: VS Code


##### プレイ動画
* 先輩に遊んでもらっている様子
    <ul class="no-bullet"><li>
    <video width="400" controls>
    <source src="/assets/movie/thythm_プレイ動画.mp4" type="video/mp4">
    </video></li></ul>


<br><br>


## ネットワーク対戦型オセロゲーム
<img src="/assets/img/othello_終了画面.png" width="500x500">

##### 概要
* 2つの端末で遊べるネットワークオセロゲーム
* Oは白，Xが黒を表す
* VS人間，VSコンピュータ どちらも可能
* コンピュータはランダムに指す
* オセロのマス目を左右にABCDEFGH，上下に12345678と表す
* 手筋を表すときには左右から先に指定（例：D3）
* ゲームプログラムは[GitHub](https://github.com/nyutonn/GameDevelopment/tree/main/2022_11_network_othello/game_main)にて公開

##### 開発期間
* 2022.10-2022.11
* 約1ヶ月

##### 使用言語・ツール
* 言語: C言語
* OS: Windows OS
* ターミナル: Windows Terminal
* エディター: VS Code

##### １つのPCを用いたプレイの仕方
* [Gitリポジトリ](https://github.com/nyutonn/GameDevelopment)をクローンする
* カレントディレクトリを以下にする`GameDevelopment/2022_11_network_othello/game_main`
* ターミナルを2つ立ち上げ，どちらもgame_mainフォルダへ移動する
 * 片方をサーバ，もう片方をクライアントとして扱う
* サーバ側で `java -jar reversi-net.jar server 3000` を実行
  * -hオプションを付けると手動で手を入力する
  * -hオプションを付けないと内部のアルゴリズムに従ってランダムより良い手を指す
  * `server`の後の`3000`はポート番号であり，サーバ側とクライアント側で同じ番号を用いること
* クライアント側で `java -jar reversi-net.jar client -h localhost 3000` を実行
  * -hオプションを付けると手動で手を入力する
  * -hオプションを付けないとランダムに手を決める

##### プレイ動画
* 人間 VS 人間
  <ul class="no-bullet"><li>
  <video width="600" controls>
  <source src="/assets/movie/othello1_手動VS手動.mp4" type="video/mp4">
  </video></li></ul>
* サーバコンピュータ VS クライアントコンピュータ
  <ul class="no-bullet"><li>
  <video width="600" controls>
  <source src="/assets/movie/othello0_自動VS自動.mp4" type="video/mp4">
  </video></li></ul>
* サーバコンピュータ VS 人間
  <ul class="no-bullet"><li>
  <video width="600" controls>
  <source src="/assets/movie/othello2_自動VS手動.mp4" type="video/mp4">
  </video></li></ul>


<br><br>


## Unity
<img src="/assets/img/unity.png" width="600x500">

##### 概要
* 多くの種類のゲームジャンルに触れることを目的に簡単なゲームを20種類ほど開発
* そのうち一部のプレイ動画を掲載
* Unityプロジェクトは一部[GitHub](https://github.com/nyutonn/GameDevelopment/tree/main/2023_3_unity_games/Program_and_Movies)にて公開

##### 開発期間
* 2022.4-2023.3
* それぞれ1日~1週間ほど

##### 使用言語・ツール
* プラットフォーム: Unity
* 言語: C#
* OS: Windows OS, macOS
* エディター: Visual Studio, VS Code

##### プレイ動画
<ul class="horizontal-list">
    <li>2Dアクション easy
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/Walk_play.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>2Dアクション difficult
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/AutoRun2d_goal.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>ツムツム
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/tumtum_play.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>エアホッケー
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/Airhockey.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>ブロック崩し
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/breakout_gameclear.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>金魚すくい
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/Goldfish_play.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>イライラ棒
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/iraira_gameclear.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>FPSアイテムゲッター
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/ItemGetter.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>ポールジャンプ
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/jumpPaul_play.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>FPS 3D迷路
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/maze_gameclear.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
<ul class="horizontal-list">
    <li>2Dシューティング
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/ShootingGame_gameclear.mp4" type="video/mp4">
        </video></li></ul>
    </li>
    <li>ストラックアウト
        <ul class="no-bullet"><li>
        <video width="350" controls>
        <source src="/assets/movie/Struckout_gameclear.mp4" type="video/mp4">
        </video></li></ul>
    </li>
</ul>
