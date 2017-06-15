---
layout: post
date: '2017-06-15 11:00 +0900'
published: true
title: HandyFlowyの推敲用スタイル「suikou」作った
tags: app workflowy
---
HandyFlowy1.5でスタイル機能がついて簡単に切り替えられるようになったので早速作ってみました。

![](https://i.gyazo.com/0cf9d1ed27e7eb4ea1ad528684ac82a5.jpg)

インデントをなくしつつ、段差はブログの見出しっぽく表現してます。見出しの付け方はハサミスクリプト準拠（子要素があるトピックを見出し化）です。

▼ CSSはこちら

    .children{padding-left:0;margin-left:0;border-left:none}.selected .project>.name,.selected .project>.notes,.selected>.children>.project .project{padding-left:0;margin-left:0}.bullet,.project.task>.name>.bullet,.project.open>.name>.bullet,.noHalo .bullet{background:none;border:none}.selected>.name>.content{font-weight:bold;font-size:100%;padding:0}.selected>.children>.project>.name>.content{font-size:20px;font-weight:bold;line-height:1.6em;margin-bottom:0.4em;padding:0;border-bottom:2px solid silver;border-radius:0}.selected>.children>.project>.children .project>.name>.content{font-size:18px;font-weight:bold;line-height:1.6em;margin-bottom:0.4em;padding:0 0 0 6px !important;border-left:4px solid silver;border-radius:0}.selected>.children>.project>.children .project>.children .project>.name>.content{font-size:16px;font-weight:bold;line-height:1.6em;margin-bottom:0.2em;padding:0 !important;border:none}.selected>.children>.project.task>.name>.content,.selected>.children>.project>.children .project.task>.name>.content,.selected>.children>.project>.children .project>.children .project.task>.name>.content{font-size:16px;font-weight:normal;margin-bottom:1em;padding:0 !important;border:none}

スタイルを取得 → http://tinyurl.com/yc93r8me

<span class="appIcon"><a href="https://itunes.apple.com/jp/app/handyflowy/id1080279196?mt=8&uo=4&at=10l4wP" target="itunes_store"><img class="appIconImg" height="100" src="http://is4.mzstatic.com/image/thumb/Purple117/v4/92/b6/df/92b6df7b-04a9-4f56-da13-59503d81691d/source/100x100bb.jpg" style="border-radius:22px;-moz-border-radius:22px;-webkit-border-radius:22px;margin: 0px 15px 1px 5px;border:none;padding:0px;float:left;"></a></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/handyflowy/id1080279196?mt=8&uo=4&at=10l4wP" target="itunes_store">HandyFlowy</a></strong></span><br><span class="appPrice">価格: 無料(記事公開時)</span><br><span class="appCategory">カテゴリ: 仕事効率化, ユーティリティ</span><br><br style="clear:both;">