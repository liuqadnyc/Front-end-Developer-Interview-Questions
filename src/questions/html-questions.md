---
title: HTML Questions
layout: layouts/page.njk
permalink: /questions/html-questions/index.html
---

* What does a `doctype` do?
* => 宣告HTML(XML)版本，不過在HTML5只剩一種版本
* How do you serve a page with content in multiple languages?
* => 通常是做成語系檔，再用PHP去讀取，不過靜態網頁也可以透過JS完成
* What kind of things must you be wary of when design or developing for multilingual sites?
* => 空間預留大小、圖片上的文字(改用前端顯示)、icon的意義
* What are `data-` attributes good for?
* => 可以記錄不太會變動的資料
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* => Semantics Tag、<video> <audio> tag、Web Worker、canvas and SVG、Offline Storage
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* => cookie: 生命週期有時效性，大小只有4KB，一般應用在帳戶自動登入。
* => sessionStorage: 當頁面關掉資料就沒了，大小有4MB，一般應用在填表單。
* => localStorage: 可以用在購物車和存一些本地數據，資料永久存在。
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
* => script直接下載並執行，且停止原本的分析。script async在背景下載，並在下載完後停止分析並執行。script defer等全部分析完再下載執行。
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
* => 因為有時候JS控制的項目如果還沒產生出來就會有錯誤，如果JS沒有操作DOM，那就可以放在head中  
* What is progressive rendering?
* => 讓display的速度越快越好，比如說display可視部分還有用defer排順序來display。
* Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
* => 因為它可以根據螢幕的解析度或圖片寬度來下載適合的圖片。
* Have you used different HTML templating languages before?
