---
title: "欢迎来到我的个人站点"
date: 2026-06-25T00:00:00+08:00
type: "home"
---

<!-- ==== HERO ==== -->
<div class="hero">
  <img src="/img/portrait.jpg" alt="头像" class="avatar">
  <h1>qiaozichen</h1>
  <p class="subtitle">AI 资产助理 • 国学·金融 • Hugo 静态站点</p>
  <a class="btn btn-primary" href="#about">了解我</a>
</div>

<!-- ==== ABOUT ==== -->
<section id="about" class="container my-5">
<h2>关于我 <img src="/img/icons/liu-xiang.svg" class="icon" alt="六爻"></h2>
<p>我是一名专注于 **A 股技术分析**、**国学奇门** 与 **AI 资产管理** 的系统化研究者。<br>
在这里，我会分享：</p>
<ul>
  <li>每日国学解读 &amp; 股票操作指引</li>
  <li>实战案例、代码片段（Python、SQL）</li>
  <li>个人项目、开源工具、学习笔记</li>
</ul>
<a class="btn btn-outline-primary" href="/about/">更多关于我 »</a>
</section>

<!-- ==== 作品展示 ==== -->
<section id="portfolio" class="container my-5">
<h2>作品展示 <img src="/img/icons/qi-gong.svg" class="icon" alt="奇门"></h2>
<div class="row">
  {{< portfolio >}}
</div>
<p class="text-center mt-3"><a class="btn btn-primary" href="/portfolio/">全部作品 »</a></p>
</section>

<!-- ==== 最新博客 ==== -->
<section id="posts" class="container my-5">
<h2>最新博客 <img src="/img/icons/wu-xing.svg" class="icon" alt="五行"></h2>

{{ range first 5 (where .Site.RegularPages "Section" "posts") }}
<div class="col-md-4 mb-4">
  <div class="card h-100">
    <div class="card-body">
      <h5 class="card-title"><a href="{{ .RelPermalink }}">{{ .Title }}</a></h5>
      <p class="card-text text-muted">{{ .Summary | plainify | truncate 80 }}</p>
    </div>
    <div class="card-footer bg-white">
      <small class="text-muted">{{ .Date.Format "2006-01-02" }}</small>
    </div>
  </div>
</div>
{{ end }}

<p class="text-center mt-4"><a class="btn btn-outline-primary" href="/posts/">查看全部博客 »</a></p>
</section>

<!-- ==== 联系方式 ==== -->
<section id="contact" class="container my-5">
<h2>联系方式</h2>
<p>如果您对我的分析、项目或合作感兴趣，欢迎通过以下方式联系：</p>
<ul>
  <li>📧 邮箱：<a href="mailto:qiaozichen@example.com">qiaozichen@example.com</a></li>
  <li>💬 微信/QQ：<code>1419818941</code></li>
  <li>🔗 Github：<a href="https://github.com/qiaozichen" target="_blank">github.com/qiaozichen</a></li>
</ul>
</section>
