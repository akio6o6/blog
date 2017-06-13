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

とのこと。オフライン対応はできると思ってなかったやつなのでビックリ。

## オフライン&高速化

さっそく試してみました。

- オフラインで起動しても直前の状態でWorkFlowyが開かれる
  - オフラインで編集→タスクキルしても編集後の文章がちゃんと残ってる
- タスクキルしてからオフラインで起動したら白紙のままで、不完全なオフライン対応なのか？と思ったんだけど、あとで試したら表示されたので、データが保存できてなかったのかも
  - 保存されてないと従来のロード画面が表示される
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

<div class="AppHtml"><span class="appIcon"><a href="https://itunes.apple.com/jp/app/handyflowy/id1080279196?mt=8&uo=4&at=10l4wP" target="_blank" rel="nofollow"><img src="http://is4.mzstatic.com/image/thumb/Purple117/v4/92/b6/df/92b6df7b-04a9-4f56-da13-59503d81691d/source/100x100bb.jpg" width="100" height="100" class="appIconImg" alt="HandyFlowy"/></a></span><br><span class="appTitle"><a href="https://itunes.apple.com/jp/app/handyflowy/id1080279196?mt=8&uo=4&at=10l4wP" target="_blank" rel="nofollow">HandyFlowy</a></span><br/><span class="appPrice">価格: 無料 (記事掲載時)</span><br/><span class="appCat">カテゴリ: 仕事効率化, ユーティリティ</span><br/><div class="appBtn"><a href="https://itunes.apple.com/jp/app/handyflowy/id1080279196?mt=8&uo=4&at=10l4wP" target="_blank" rel="nofollow">AppStoreでチェック</a></div></div>
