---
layout: post
date: '2017-08-07 11:50 +0900'
published: true
title: JekyllでTwitter cardのサムネイル画像を設定する
tags: jekyll
---
Twitter cardで見た時にデフォルトも味気ないし、
サムネあった方がいいと思いやってみた。

▼ 参照

* [Jekyllでサムネイル画像を実装する - totorajの開発日記](http://tj.hateblo.jp/entry/2016/09/20/223029)
* [Support for the Summary Twitter Card in Jekyll](https://gist.github.com/davidensinger/5415639)

以下のコードをヘッダーに書いて（`_includes/meta.html`など経由してもOK）、

```
{% if page.thumb %}
  <meta name="twitter:image" content="{{ page.thumb }}" />
{% else %}
  <meta name="twitter:image" content="logo.png（デフォルト用の画像URL）" />
{% endif %}
```

記事ファイルのFront Matterに「thumb」という項目を作り、そこに画像URLを書けばOK。

最近（一昔前？）の流行り的にはindex（トップ画面）にサムネイルを表示するのもありだよなーと思いつつ、あんま設定することはない気がするのでとりあえずテキストオンリーでやってく。