---
layout: post
date: '2017-04-15 15:23 +0900'
published: true
title: WorkflowとGit2Goを使ってJekyllでモブログする
tags: moblog workflow jekyll
---
やりたくなっちゃうよね。

私はスマホからブログを更新したい人なんだけど、Jekyll （+ GitHub Pages ）には当然アプリがない。ってことで GitHub にコミットできるアプリをもろもろ試した。

で、一番使いやすかったのは **Git2Go** だった。

<span class="appIcon"><a href="https://itunes.apple.com/jp/app/git2go-git%E3%82%AF%E3%83%A9%E3%82%A4%E3%82%A2%E3%83%B3%E3%83%88/id963577401?mt=8&uo=4&at=10l4wP" target="itunes_store"><img class="appIconImg" height="100" src="http://is1.mzstatic.com/image/thumb/Purple71/v4/4d/31/33/4d31339b-cbd1-7998-453a-25839e699cea/source/100x100bb.jpg" style="border-radius:22px;-moz-border-radius:22px;-webkit-border-radius:22px;margin: 0px 15px 1px 5px;border:none;padding:0px;float:left;"></a></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/git2go-git%E3%82%AF%E3%83%A9%E3%82%A4%E3%82%A2%E3%83%B3%E3%83%88/id963577401?mt=8&uo=4&at=10l4wP" target="itunes_store">Git2Go – Gitクライアント</a></strong></span><br><span class="appPrice">価格: 無料(記事公開時)</span><br><span class="appCategory">カテゴリ: 仕事効率化, ビジネス</span><br><br style="clear:both;">

操作が直感的だったり、Open in で他所からファイルを読み込めたり、URLスキームから投稿できたりと優秀。スマホからはファイルの追加や細かい修正ができればいいので単体でも充分使える。しかも無料。

Git2Go だけでも便利なんだけど、投稿の際に Front-matter（投稿のタイトルやタグをつけるためのフォーム）を付けるのが若干めんどい。ので Workflow（最近Appleに買収されたオートメーションアプリ） と組み合わせて使ういいと思う。

<span class="appIcon"><a href="https://itunes.apple.com/jp/app/workflow-powerful-automation-made-simple/id915249334?mt=8&uo=4&at=10l4wP" target="itunes_store"><img class="appIconImg" height="100" src="http://is1.mzstatic.com/image/thumb/Purple111/v4/19/ce/ee/19ceeeb1-fb84-2e82-2474-421fdeb936fc/source/100x100bb.jpg" style="border-radius:22px;-moz-border-radius:22px;-webkit-border-radius:22px;margin: 0px 15px 1px 5px;border:none;padding:0px;float:left;"></a></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/workflow-powerful-automation-made-simple/id915249334?mt=8&uo=4&at=10l4wP" target="itunes_store">Workflow: Powerful Automation Made Simple</a></strong></span><br><span class="appPrice">価格: 無料(記事公開時)</span><br><span class="appCategory">カテゴリ: 仕事効率化, ユーティリティ</span><br><br style="clear:both;">

その Workflow で Jekyll 仕様の Front-matter を先頭に追加→.mdファイル化するワークフローを作った。（Workflow のワークフローって表現できる日本語ありがたい:) ）

<div style='max-width:400px;background:#2B5ED5;padding:10px;margin:16px 0;border-radius:4px;'><a href='https://workflow.is/workflows/e133067dbb89466692b763e138823315' style='color:white;text-decoration:none;'><img width='100' height='100' align='left' src='https://workflow-gallery.s3.amazonaws.com/workflow_icons/e133067dbb89466692b763e138823315.png' style='padding:0px;border:none;'><span style='font-size:120%;margin:10px;'>Commit-text-Jekyll</span><br><div style='float:left;color:white;background:#163F9F;margin:4px;padding:4px 10px;border-radius:50px;'>GET WORKFLOW</div></a><br clear='all'></div>

手順は

0. 記事を書く
1. お気に入りのエディタからワークフローを実行
2. タイトルとタグを手動で入力
3. 最後の Open in で Git2Go を選択
4. 投稿用ファイル置き場に書き出す
5. コミット
6. プッシュ

で更新できる。

Git2Go のURLスキームならリポジトリとファイルの場所を指定できて楽なんだけど、URLスキームだと文中に`&`が使えなかったりエンコードめんどかったりするので「Open in」から Git2Go を選択して、ファイルの場所は後から指定することにした。