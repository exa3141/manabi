---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "集合論入門 集合とその性質"
subtitle: ""
summary: ""
authors:
- admin
tags:
-  "数学"
categories: 
- "集合論"
date: 2022-04-17T13:23:19+09:00
lastmod: 2022-04-17T13:23:19+09:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

集合は現代の数学を形作っている。どんなものも所詮集合に過ぎない。

## 集合とは

<blockquote class="callout_definition">
        <h4>定義: 集合</h4>
集合とは、ものの集まりである。
</blockquote>


<blockquote class="callout_definition">
        <h4>定義: 元</h4>
ある集合を構成している「もの」のことを集合の「元」または「要素」と呼ぶ。
</blockquote>

ここでいう「もの」はなんでもいい。関数や数のような数学的な対象を考えてもいいし、今私の机の上にあるペン全体の集合というものも考えられる。
しかし、ある集合にその要素が入るか入らないかは厳密に定められていなければならない。
「100億より大きい実数の集合」は考えられるが、「なんかデカい数の集合」というのは考えることができない。

とはいうものの、集合自体は「ものの集まり」というなんともふんわりした言葉で定義されているのは気になる。
実は、「自身を含まないがこの世にあるすべての集合を集めた集合」というものを考えると[パラドックス](https://ja.wikipedia.org/wiki/%E3%83%A9%E3%83%83%E3%82%BB%E3%83%AB%E3%81%AE%E3%83%91%E3%83%A9%E3%83%89%E3%83%83%E3%82%AF%E3%82%B9)が生じる。
したがって単なる「ものの集まり」という定義は不十分であるといえる。
これを回避しつつ集合論を組み立てることもできるようだが、難しいのでこのへんはごまかしつつ先に進む。

<blockquote class="callout_definition">
        <h4>定義: 属する</h4>
ある「もの」\(x\) が集合 \(A\) の元であるとき、「\(x\) は \(A\) に属する」または「\(x\) は \(A\) に含まれる」または \( x \in A \) と表現する。
</blockquote>

ある元がある集合に含まれるか含まれないかは厳密に定められるので \\(x \in A\\) または \\( x \not \in A \\) のどちらかは必ず成立する。成立するかわからないとなったときには、もう \\( A \\) は集合ではないとわかる。

## 記法

<blockquote class="callout_others">
        <h4>外延的記法</h4>
集合を、元を具体的に並べて示したものを集合の外延的記法という。
<div class="suushiki">$$ A=\{i,l,o,v,e,u,\cdots\} $$</div>
</blockquote>

集合をその中身を記して表現しようとするのは自然であるが、当然すべて書き並べるわけにはいかない場合が多い。そんなあなたに内包的記法。

<blockquote class="callout_others">
        <h4>内包的記法</h4>
集合を、その元が満たす命題により示したものを集合の内包的記法という。
<div class="suushiki">$$ A=\{ x | P(x) \} $$</div>
ただし\( P(x) \) は \(x\) についての命題。たとえば「\(x\)は実数」など。
</blockquote>

このように定義された集合では、要素を一つ一つチェックしていかなくても命題 \\(P\\) さえチェックすればある元が含まれるか含まれないかを判定することができる。

## 空集合

<blockquote class="callout_definition">
        <h4>定義: 空集合</h4>
要素を一つももたない集合を空集合と呼び、\( \emptyset \) や \( \varnothing \) で表す。
</blockquote>

内包的記法を考えると、集合 \\(A\\) の要素は命題 \\(P\\) が真になるような \\(x\\) のすべてであることがわかるが、命題によってはそのような \\(x\\) が存在しないことがある。そのような場合に限って \\(A\\) を集合としないのは不自然であるから、要素が一つもない集合というのも考える。これが空集合である。

いうなれば、集合は「ものの集まり」というより「その要素が属するか属さないかが厳密に定められているもの」である。このような認識で集合を考えれば空集合の概念も自然に感じられよう。

## 部分集合

<blockquote class="callout_definition">
        <h4>定義: 部分集合</h4>
\( A \subset B \; \Longleftrightarrow \) \(A\) は \(B\) の部分集合である \(\Longleftrightarrow\) \(A\) は \(B\) に包まれる 

\\(\overset{\text{def}}{\Longleftrightarrow}\\) 
<div class="suushiki">任意の \(x\) について \(x \in A \Rightarrow x \in B \)</div>
</blockquote>

ある集まりを考えるとき、その部分について考えることがよくある。人間が考える「部分」という感覚を数学的に表すと、部分に含まれるものは絶対に全体にも含まれているよね、ということである。人間のあやふやな感覚をかっちり論理で定義していくことができるというのは集合論の醍醐味である。

ここで、空集合と部分集合について考えてみる。空集合はなにかの集合の部分集合たりえるのだろうか。空集合は部分集合をもつのだろうか。
定義に戻って考えてみるとこの疑問に答えることができる。数学では定義に戻って考えることが非常に有効である。

空集合は要素を一つももたない集合であるから言うなれば最も"小さい"集合である。したがって任意の集合 \\(A\\) に対して

<div class="suushiki"> $$ \varnothing \subset A $$ </div>

が成り立つと予想するかもしれない。部分集合の定義からこれは「\\(x \in \varnothing \Rightarrow x \in A \\)」と同値である。
今、任意の \\(x\\) について \\(x \in \varnothing \\) はつねに偽であるから \\(x \in \varnothing \Rightarrow x \in A \\) は[真になる。]({{< relref "/post/naraba" >}})
したがって

## 集合の相等

<blockquote class="callout_definition">
        <h4>定義: 集合の相等</h4>
\( A = B \; \Longleftrightarrow \) \(A\) と \(B\) は等しい

\\(\overset{\text{def}}{\Longleftrightarrow}\\) 
<div class="suushiki">任意の \(x\) について \(x \in A \Leftrightarrow x \in B \)</div>

\\(\Longleftrightarrow\\)
<div class="suushiki">\(A \subset B \) かつ \(A \supset B \)</div>
</blockquote>

ある集合とある集合が同じということは、その集合の要素が属するか属さないかの命題・条件が等しいということである。それを考えると \\(x \in A \Leftrightarrow x \in B \\) が相等の条件になるのは納得できる。

特筆すべきなのは、\\(x \in A \Leftrightarrow x \in B \\)という条件が\\(A \subset B \\) かつ \\(A \supset B \\) という条件と同値であるということである。これは部分集合の定義を使えば直ちに導くことができる。多くの証明では\\(A \subset B \\) かつ \\(A \supset B \\) を示すことによって \\(A=B\\) の証明としているが、これは単に \\(x \in A \Leftrightarrow x \in B \\) の両矢印を分けて証明しているだけであって、特に深い意味はない。