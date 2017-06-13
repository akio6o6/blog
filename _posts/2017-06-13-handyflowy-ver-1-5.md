---
layout: post
date: '2017-06-13 17:00 +0900'
published: true
title: HandyFlowyがVer.1.5でオフラインに対応したんですって
tags: app workflowy
---
ワオ。

AppStoreでのアプデ説明は、

- オフラインに対応
- 起動の高速化
- スタイル機能の追加
- その他、多くの機能を改善しました。

とのこと。オフライン対応はできると思ってなかったのでビックリ。

## オフライン&高速化

さっそく試してみました。

- オフラインで起動しても直前の状態でWorkFlowyが開かれる
  - オフラインで編集→タスクキルしても編集後の文章がちゃんと残ってる
- タスクキルしてからオフラインで起動したら白紙のままで、不完全なオフライン対応なのか？と思ったんだけど、あとでもう一度オフラインで起動したら読み込まれたので、まだデータが保存できてなかったのかも
  - ローカルに保存されてないと従来のロード画面が表示されるっっぽい
- 起動は驚異的に早くなってる
  - ~1.4 「HandyFlowyのスプラッシュ」→「HandyFlowyのロード」→「WorkFlowyのロード」→「表示」
  - 1.5 「HandyFlowyのスプラッシュ」→「HandyFlowyのロード」→「表示」
  - 文量多いと「WorkFlowyのロード」が長くなるので、ここが省略されるとだいぶ違う。

この機能追加のおかげで公式アプリがとうとうお役御免になりそうです。
どうやってるんだろ？ちょくちょくローカルにWorkFlowyの状態を保存して、起動時にはそっちを読み込んでからWorkFlowyと同期って感じ？

## スタイル機能

今まではスタイルを変更するためには拡張機能スクリプトを利用するか、あらかじめ設定で変更できるフォントサイズや背景を弄るしかなかったんですが、

今回のアップデートで設定のスタイルにCSSを直接書けるようになりました。ChromeやFirefoxでおなじみのStylishっぽく使える感じです。

スタイルを切り替えたい時に「スライドでメニュー呼び出し」→「スタイルをタップ」という短いステップでスタイルを変更できるようになりました。自作の「[suikou](http://akio6o6.hateblo.jp/entry/2016/04/02/000000)」なんかの出番が増えるかもしれません。

---

ほかにもパワーアップしてるらしいのでこれからいろいろ触ってみまーす。

<div id="appreach-box" style="text-align:left;">
    <img id="appreach-image" src="//lh3.googleusercontent.com/V1eCKX02a-G7Cyr5J2O4LkX1afocZIkJRgQtP5dJfE1cHjDH8dJpRPohppEgairMpe-q=w170" alt="HandyFlowy" style="float:left; margin:10px; width:25%; max-width:120px; border-radius:10%;">
    <div class="appreach-info" style="margin: 10px;">
        <div id="appreach-appname">HandyFlowy</div>
        <div id="appreach-developer" style="font-size:80%; display:inline-block; _display:inline;">
            開発元:<a id="appreach-developerurl" href="https://itunes.apple.com/jp/developer/michinari-yamamoto/id967739756?uo=4" target="_blank" rel="nofollow">Michinari YAMAMOTO</a>
        </div>
        <div id="appreach-price" style="font-size:80%; display:inline-block; _display:inline;">無料</div>
        <div class="appreach-powered" style="font-size:80%; display:inline-block; _display:inline;">
            posted with <a href="http://mama-hack.com/app-reach/" title="アプリーチ" target="_blank" rel="nofollow">アプリーチ</a>
        </div>
        <div class="appreach-links" style="float: left;">
            <div id="appreach-itunes-link" style="display: inline-block; _display: inline;">
                <a id="appreach-itunes" href="https://itunes.apple.com/jp/app/handyflowy/id1080279196?mt=8&amp;uo=4&amp;at=10l4wP" target="_blank" rel="nofollow">
                    <img src="https://nabettu.github.io/appreach/img/itune_ja.svg" style="height:40px;">
                </a>
            </div>
            <div id="appreach-gplay-link" style="display:inline-block; _display:inline;">
                <a id="appreach-gplay" href="https://play.google.com/store/apps/details?id=jp.nap.app.handyflowy" target="_blank" rel="nofollow">
                    <img src="https://nabettu.github.io/appreach/img/gplay_ja.png" style="height:40px;">
                </a>
            </div>
        </div>
    </div>
    <div class="appreach-footer" style="margin-bottom:10px; clear: left;"></div>
</div>
