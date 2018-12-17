---
title: "Pythonを勉強してみる:PyGame編"
date: 2018-12-20T12:00:00+07:00
draft: false

categories:
- 開発
tags:
- 開発
- Python
keywords:
- python
- Python3
- pygame
- PySDL2

summary: "Python入門としてPyGameを勉強しようと思ったけど、どうしようか迷ったという話。"

---

突然ですが、実は私開発スキルの幅がかなーり少なく、まともにできるのはAndroidネイティブ開発とUnity用いたスマートフォンアプリ開発ぐらいだったりします。

<span class="large b">こりゃやべえ</span>ってなったので今Web側で需要がありそうな言語調べてPythonの勉強初めてみました。

# Pythonの勉強について
とりあえず<b>無料</b>で勉強したかったので、<a href="https://paiza.jp/works/">paizaラーニング</a>にて`Python3`を勉強してみることに…。

3って何？2もあるの？？というレベルの初心者ですが一応paizaの`Python3`コースは一通り完了。ただ<b>最低限の文法が覚えた気がするけど、実用できる気が一切しない</b>。

ということで、元々スマホゲームアプリは作りなれているのもあり、「勉強がてらPCで動くミニゲーム作ってみよう」となりました。そしてその結果「Pythonでゲーム開発するなら<a href="http://www.pygame.org/hifi.html">pygame</a>」を使うらしい、という情報をGETしました。

## pygameの勉強について

なにやらpygameは長年Pythonユーザーに親しまれてきたゲーム開発用のライブラリとのこと。
特に疑うこともなく、「へー」と思いながらpygameを触ってみることに。

で、さっそくpygameでHellowWorld作ったり、画像表示、キー入力サンプル作ってキャッキャしてた時に<a href="http://gamepro.blog.jp/python/pygame/introduction">とあるサイト</a>で衝撃の文章が…。

> Pygameは、Pythonのゲーム制作用モジュールです。
>
> 主にコンピュータグラフィクスと音声を扱うための機能が備わっています。
>
> このライブラリは複数のプラットフォームで統一的に使えるSDLというマルチメディアAPIライブラリから作られています。
>
> よって、Pygameで作られたゲームはWindows、Mac、Linux上で動かすことが出来ます。
>
> ただし、現在は開発が停止しています。(後継ライブラリはPySDL2)

…あれ？

> <span class="large"> ただし、現在は開発が停止しています。(後継ライブラリはPySDL2)</span>

oh...  
pygame、開発終了してるやん。  
というより後継ライブラリがいるって事はpygameもう使わない方が良いってことでは…？

---

一応本当にpygame使わない方が良いの？という視点で調べて見たのですが…<br><br>

1. PyGameの最新版は2009年8月にリリース。
2. = Python3未対応
3. = 64bit未対応

とのこと。

---

ということでpygameの勉強は中止して、今後は<span class="red b">PySDL2について調べてみようかな？</span>と思ったけどpygameの公式サイトを見てみると思わぬ更新が。

<br><a href="https://www.pygame.org/news/2018/7/pygame-1-9-4-released">pygame 1.9.4 released — 19 Jul, 2018</a>

<br><span class="large b">pygame、普通に更新来てた。</span><br><br>

しかもちゃんとPython3.7対応してるっぽいです。


## まとめ
結局pygameとPySDL2どっち使おうかな？というのは今度調べてみます。ただそもそもPython詳しくないんで、最新のpygameが使いづらくなってるとかじゃなければ<b>昔から存在する＝情報が探しやすい</b>pygameを使う可能性が高めかな〜と思っています。
