---
title: "【pygame】Python3を勉強する際、どのライブラリを使うべきか悩んだ話"
date: 2018-12-19T12:00:00+07:00
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

summary: "Python入門としてPyGameを勉強しようと思ったけど、どうしようかな…と迷ったという話。pygameが今のゲーム開発にライブラリとして適任なのか調べてみました。"

thumbnailImagePosition: "left"
thumbnailImage: https://user-images.githubusercontent.com/8590431/50209656-e43a6f00-03a6-11e9-990b-32ea3538f849.png

---

## Pythonを勉強しよう
<img height="300" src="https://user-images.githubusercontent.com/8590431/50209656-e43a6f00-03a6-11e9-990b-32ea3538f849.png">


突然ですが、実は私開発スキルの幅がかなーり少なく、まともにできるのはAndroidネイティブ開発とUnity用いたスマートフォンアプリ開発ぐらいだったりします。

<span class="large b">こりゃやべえ</span>ってなったので今Web側で需要がありそうな言語調べてPythonの勉強初めてみました。

### なぜPython?
そもそもなぜ数ある言語の中からPythonを選んだかが、ですがいくつかの理由があります。

まず、自分がスマホのクライアント開発しか出来ない状態なのでWeb側で使える言語を探していました。
また以前から地味に気になっていた<span class="b red">機械学習等にPythonが非常に向いている</span>点、かつ<span class="b red">海外では一般的にRubyよりPythonのほうが需要がある</span>と聞き、Pythonの勉強を始めることにしました。

### 私が選んだPythonの勉強方法
とりあえず何はともあれ<span class="b">無料</span>で勉強したかったので、<a href="https://paiza.jp/works/">paizaラーニング</a>にて`Python3`を勉強してみることに…。

3って何？2もあるの？？というレベルの初心者ですが一応paizaの`Python3`コースは一通り完了。ただ<span class="red b">最低限の文法が覚えた気がするけど、実用できる気が一切しない…</span>。

ということで、元々スマホゲームアプリは作りなれているのもあって<span class="b">「勉強がてらPCで動くミニゲーム作ってみよう」</span>という結論に至りました。

そしてその結果<span class="b">「Pythonでゲーム開発するなら<a href="http://www.pygame.org/hifi.html">pygame</a>」を使うと良いらしい</span>、という情報をGETしました。

### pygameの勉強しようとして気がついたこと

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

> <span class="large red b"> ただし、現在は開発が停止しています。(後継ライブラリはPySDL2)</span>

oh...  
pygame、開発終了してるやん。  
というより後継ライブラリがいるって事はpygameもう使わない方が良いってことでは…？

#### pygameを使わない方が良い理由

一応本当にpygame使わない方が良いの？という視点で調べて見たのですが…<br><br>

1. pygameの最新版は2009年8月にリリース。
2. = Python3未対応
3. = 64bit未対応

とのこと。

### pygame公式で更新が… @ 7月2018年
ということでpygameの勉強は中止して、今後は<span class="red b">PySDL2について調べてみようかな？</span>と思ったけどpygameの公式サイトを見てみると思わぬ更新が。

<img height="400" alt="”pygameの更新履歴" title=”pygameの更新履歴" src="https://user-images.githubusercontent.com/8590431/50209432-49419500-03a6-11e9-9544-7493ae9eb9b4.png">

<br><a href="https://www.pygame.org/news/2018/7/pygame-1-9-4-released">pygame 1.9.4 released — 19 Jul, 2018</a>

<br><span class="large b">pygame、普通に更新来てた。</span><br><br>

しかもちゃんとPython3.7対応してるっぽいです。

コレ見る限り、pygameを使うこと自体は特に問題なさそうですね。

## まとめ
結局pygameとPySDL2どっち使おうかな？というのはまた今度調べてみます。

ただそもそもPytho自体詳しくないので、最新のpygameが使いづらくなってるとかじゃなければ<span class="b red">昔から存在する＝情報が探しやすいpygameの方</span>を使う可能性が高めかな〜と思っています。
