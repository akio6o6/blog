---
layout: post
date: '2017-09-15 10:00 +0900'
published: true
title: ScrapboxからMarkdownに変換しつつTextwellに送信するBookmarklet
tags: moblog scrapbox
---
作りました。

▼ コードはこちら

    javascript:(function(){var i=function(a){a=a.replace(/&/g,"&amp;");a=a.replace(/</g,"&lt;");a=a.replace(/>/g,"&gt;");a=a.replace(/"/g,"&quot;");return a=a.replace(/'/g,"&#39;")},g=function(d){d=void 0===d?0:d;for(var f="",h=1;h<d;h++){f+=" "}return f},e=function(k){k=void 0===k?"":k;var l=document.createElement("div");l.innerHTML=k;k=l.querySelectorAll("strong");for(var n=0;n<k.length;n++){for(var w=k[n],q=+w.className.split("level-")[1],r=w.innerHTML,q=void 0===q?1:q,q=5-q,p="",m=0;m<q;m++){p+="#"}w.innerHTML=p+" "+r}return l.innerHTML},c=function(h){h=void 0===h?"":h;var k=document.createElement("div");k.innerHTML=h;h=k.querySelectorAll("a");for(var l=0;l<h.length;l++){var q=h[l],n=q.innerText.trim(),p=q.href,n="["+n+"]("+p+")",m=q.querySelector("img");null!==m&&(n="[![Image]("+m.src+")]("+p+")");q.innerText=n}return k.innerText},t=document.querySelector(".lines"),b=t.querySelector(".line-title .text").innerText,t=t.querySelectorAll(".line");pageTexts=[];for(var j=1;j<t.length;j++){for(var u=t[j].querySelector(".text").cloneNode(!0),s=u.querySelectorAll("span.empty-char-index"),v=0;v<s.length;v++){var o=s[v];o.innerText=""}s=u.querySelectorAll("span.backquote");for(v=0;v<s.length;v++){o=s[v],o.innerText="`"}v=u.innerHTML.replace(/<span>/g,"");v=v.replace(/<span.+?>/g,"").replace(/<\/span>/g,"");v=v.replace(/<br.+?>/g,"");v=v.replace(/\n/gi,"").replace(/\t/gi,"").trim();v=e(v);v=c(v);u=u.querySelector(".indent-mark");null!==u&&(o=+u.style.width.split("em")[0]/1.5,v=g(o)+"- "+v);null===u&&0<v.length&&"#"!==v[0]&&(v+="");pageTexts.push(v)}(function(f,h){f=void 0===f?"Title":f;h=void 0===h?[]:h;for(var k="# "+f+"\n",l=0;l<h.length;l++){k+="\n"+h[l]}location.href="textwell://replace?text="+encodeURIComponent(i(k))})(b,pageTexts)})();


daiizさんの作った「[ScrapboxコンテンツをMarkdownに変換するBookmarklet](https://scrapbox.io/daiiz/Scrapbox%E3%82%B3%E3%83%B3%E3%83%86%E3%83%B3%E3%83%84%E3%82%92Markdown%E3%81%AB%E5%A4%89%E6%8F%9B%E3%81%99%E3%82%8BBookmarklet)」を参考にしつつ、見出しのルールなどを自分仕様（太字レベル3をh2扱いなど）にして作成しました。

メモはScrapboxで取りたいけど、MarkdownやHTMLの編集→各種サービスへの投稿はTextwellでやりたい人向けのニッチなBookmarkletになってます。

ちなみに、[Safari Snippets](https://itunes.apple.com/jp/app/safari-snippets/id1126048257?mt=8) というExtensionからスクリプトを実行できるアプリを使えば [91958](https://itunes.apple.com/jp/app/91958/id1257585182?mt=8) や他のブラウザでもScrapboxからTextwellに送信できます。オススメ。