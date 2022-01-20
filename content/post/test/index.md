---
title: 線形写像とは
subtitle: 線形写像を解説

# Summary for listings and search engines
summary: 線形性を満たす関数・写像を線形写像という。任意の行列は線形写像を表す。同時に任意の線形写像は行列で表現できる。

# Link this post with a project
projects: []

# Date published
date: "2020-12-13T00:00:00Z"

# Date updated
lastmod: "2020-12-13T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  #caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- 大学教養
- 定義の解説

categories:
- 代数学-線形代数学
---

## 線形写像の定義

線形写像とは何であろうか。定義をみていく。

<blockquote class="callout_definition">
        <h5>定義: 線形写像</h5>
$\boldsymbol{x},\boldsymbol{y}$ は $n$ 次ベクトル、$k$ はスカラーとする。このとき、
<div class="suushiki">
$$
\text{写像}T:\mathbb{C}^n \to \mathbb{C}^m \text{が線形写像である} \overset{\text{def}}{\iff}
\left\{ \,
    \begin{aligned}
    & T(\boldsymbol{x}+\boldsymbol{y})=T(\boldsymbol{x})+T(\boldsymbol{y}) \\
    & T(k\boldsymbol{x})=kT(\boldsymbol{x})
    \end{aligned}
\right.
$$
</div>

と定義する。</blockquote>

<div class="suushiki" >
$$
\text{写像}T:\mathbb{C}^n \to \mathbb{C}^m \text{が線形写像である} \overset{\text{def}}{\iff}
\left\{ \,
    \begin{aligned}
    & T(\boldsymbol{x}+\boldsymbol{y})=T(\boldsymbol{x})+T(\boldsymbol{y}) \\
    & T(k\boldsymbol{x})=kT(\boldsymbol{x})
    \end{aligned}
\right.
$$
</div>