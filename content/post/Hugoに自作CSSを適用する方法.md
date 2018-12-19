---
title: "【初心者用】Hugoで作成したブログに自作CSSを適応する簡単な方法【CSS】"
date: 2018-12-15T12:38:33+07:00
draft: false

categories:
- 開発
tags:
- 開発
- Hugo
- CSS
keywords:
- Hugo
- CSS
- ブログ

thumbnailImagePosition: "left"
thumbnailImage: https://user-images.githubusercontent.com/8590431/49916201-68cf4e00-fecc-11e8-85a6-73fc7b435f57.png

summary: "Hugoで作成したウェブページに自作CSSを反映させる方法についてまとめました。予想以上に簡単にできたため、CSSに詳しくない方も是非試してみてください！"

---

## CSSの反映が簡単に出来た件
<a href="../hugo-github-pagesでブログ作成してみた件/">以前</a>Hugoでブログはじめました～！って時に<b>色の付け方がわからない</b>とか言ってましたが、思ったより簡単に出来たので方法をまとめておきます。<br>
<span class="gray small"><b>以前の記事で触れてたフォントの変更方法もわかったけど、そもそも使いたいフォントを探していないので今回はスルーします。（）</b></span>

### 自作CSSを適用するために必要なもの
1. 自作CSS<br>
以上。

今回は以下な感じでどシンプルなCSSを書いてみました。

``` CSS
/*
Basic CSS for Text related things.

Color info
https://www.wanichan.com/web/resources/color.html
*/
span.b { font-weight: bold; }

span.red { color: orangered; }
span.gray { color: darkgray; }

span.large { font-size: 1.5em; }
span.small { font-size: 0.75em; }

span.ul { border-bottom: solid 3px;}
span.ul-red { border-bottom: solid 3px orangered;}
span.ul-gray { border-bottom: solid 3px darkgray;}
span.dul { border-bottom: dotted 3px;}
span.slash { text-decoration: line-through; }
```
### 自作CSSを適用する方法
1. プロジェクト直下の`static`フォルダ配下にCSSファイルを配置する。
    - 画像ファイル等を置いている`static`フォルダを同じ場所です。
2. `themes`以下で`CSS`を取り込んでいる`html`ファイルを検索する。
    - `<link rel="stylesheet" href="`で検索し、他の`CSS`を取り込んでいる場所を探しました。
    - そこに自作した`CSS`を取り込むコードを以下のように記述するだけで、一瞬で反映されます。

CSSを取り込むコードのサンプル

``` html
<!--CUSTOM STYLES-->
<link rel="stylesheet" href="/css/nc-text.css" />
<!--CUSTOM STYLES END-->
```

※さも今後複数の`CSS`を追加するかのようなコメントつけてますが、正直そこまで`CSS`を実装/調整することはないかなと思います…。

## まとめ
ウェブ側のお約束だったりサーバー側の知識が皆無なので、`CSS`とか使った調整はあまり考えていなかったのですが、あまりにも簡単に調整できてびっくりです。

今後余裕があればちょこちょこカスタマイズしていきたいなーと思っています。

まだ触って一週間程度だけど、<span class="b">Hugoさん思ってた以上に便利</span>でびっくり。
