---
layout: post
date: '2017-03-28 13:00 +0900'
published: true
title: Prose から Jekyll に投稿するための設定
tags: jekyll
---
GitHub Pages というか Jekyll に楽に投稿したくて「<a href="http://prose.io" target="_blank">Prose</a>」を使うことにした。Prose は GitHub をブラウザから編集するクライアントで、MarkDown記法が挿入しやすかったり、画像をドラッグ・アンド・ドロップでアップロードできる便利なサービス。

んで、そっから Jekyll を扱う場合はリポジトリの `_config.yml` に Prose 用の設定を書く必要があるんだけど、

いい感じにできたのでメモしておく。

```
prose:
  # rooturl: '_posts'
  siteurl: 'http://USERNAME.github.io/' 
  media: 'media'
  metadata:
    _posts:
      - name: "layout"
        field:
          element: "hidden"
          value: "post"
      - name: "title"
        field:
          label: "title"
          element: "text"
          value: ""
      - name: "tags"
        field:
          label: "tags"
          element: "text"
          value: ""
      - name: "date"
        field
          label: "date"
          element: "text"
          value: ""
      - name: "published"
        field:
          label: "publish"
          element: "checkbox"
          value: "true"
```

コミットした後に再読み込みしないと投稿されないのでなんとかしたい。

▼ 参考

* <a href="https://github.com/prose/prose/wiki/Prose-Configuration" target="_blank">Prose Configuration · prose/prose Wiki</a>（公式）
* <a href="http://www.bokukoko.info/entry/2015/03/26/%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9E%E3%81%A7%E3%82%82%E3%82%AA%E3%82%B9%E3%82%B9%E3%83%A1%EF%BC%81_Prose_%E3%81%A7_Jekyll_%E3%81%AE%E8%A8%98%E4%BA%8B%E3%82%92%E7%AE%A1%E7%90%86%E3%81%99" target="_blank">プログラマでもオススメ！ Prose で Jekyll の記事を管理する - ボクココ</a>
