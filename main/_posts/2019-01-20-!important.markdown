---
layout: post
title:  "!Important directive"
date:   2019-01-20 12:00:00 +0900
comments: true
categories: JavaScript
---

So it was just an ordinary day of grappling with JavaScript and CSS. I wanted to apply to a DOM element certain sizes of width and height; I made a new class in CSS file, and set width and height values the element needed to be applied. But the style was not applying the width and height values I set for, while other values were normally applied. A senior told me that I can make use the !important rule in that case, and here is the posting related to it.

In this posting I will briefly introduce !important and some things worth noting.
https://css-tricks.com/when-using-important-is-the-right-choice/
https://www.lifewire.com/what-does-important-mean-in-css-3466876


1. What does "!important" do?
- In short, it is a rule that makes a certain styling property ALWAYS APPLIED first. A rule that has !important will take over the top priority over any other properties in the CSS document.

<div class="colorscripter-code" style="color:#f0f0f0; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important; overflow:auto"><table class="colorscripter-code-table" style="margin:0; padding:0; border:none; background-color:#272727; border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px; border-right:2px solid #4f4f4f"><div style="margin:0; padding:0; word-break:normal; text-align:right; color:#aaa; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div><div style="line-height:130%">4</div></div></td><td style="padding:6px 0"><div style="margin:0; padding:0; color:#f0f0f0; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%">.example&nbsp;{width:150px;&nbsp;height:150px;&nbsp;background:#9bbf42}</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&lt;div&nbsp;class="example"&nbsp;style="width:100px;&nbsp;height:100px;&nbsp;background:#4fa5ff"&gt;Hello&lt;/div&gt;</div></div></td><td style="vertical-align:bottom; padding:0 2px 4px 0"><a href="http://colorscripter.com/info#e" target="_blank" style="text-decoration:none; color:white"><span style="font-size:9px; word-break:normal; background-color:#4f4f4f; color:white; border-radius:10px; padding:1px">cs</span></a></td></tr></table></div>
![img]({{ "/assets/img/blue.png" | absolute_url }})

- [When !important is NOT applied]


<div class="colorscripter-code" style="color:#f0f0f0; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important; overflow:auto"><table class="colorscripter-code-table" style="margin:0; padding:0; border:none; background-color:#272727; border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px; border-right:2px solid #4f4f4f"><div style="margin:0; padding:0; word-break:normal; text-align:right; color:#aaa; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div><div style="line-height:130%">4</div></div></td><td style="padding:6px 0"><div style="margin:0; padding:0; color:#f0f0f0; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%">.example&nbsp;{width:150px;&nbsp;height:150px;&nbsp;background:#1f1f1f&nbsp;!important;&nbsp;}</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&lt;div&nbsp;class="example"&nbsp;style="width:100px;&nbsp;height:100px;&nbsp;background:#4fa5ff"&gt;Hello&lt;/div&gt;</div></div></td><td style="vertical-align:bottom; padding:0 2px 4px 0"><a href="http://colorscripter.com/info#e" target="_blank" style="text-decoration:none; color:white"><span style="font-size:9px; word-break:normal; background-color:#4f4f4f; color:white; border-radius:10px; padding:1px">cs</span></a></td></tr></table></div>
![img]({{ "/assets/img/green.png" | absolute_url }})

- [When !important is applied] 
- As can be seen, it overwrites what is specified within the <div> tag. The job is accomplished, and I made it..! But.. really?



2. Some concerns on when to and when not to use it

- CSS is an abbreviation for Cascading Stlying Sheet. By 'cascading', it means the elements that comprises document will be in particular order so that they will be applied with the order; hence the thing that is written most recently will be applied. From the above example, the style of <div> was written after the class 'example', hence overwrting what is written inside of the class. 

- However !important directive is always applied no matter where the rule appears in the CSS document. It is recommended to be used ONLY FOR TESTING purpose, to check if a CSS issue is from a specificity issue. If one depends too heavily on the !important declaration to achieve a desired style, one will eventually have a style sheet littered with all !important styles here and there.

- This !important directive has other important motive; to help web page users deal with style sheets that make pages difficult for them to use or read. If a user marks a style as !important, that style overrules the web page author's style sheet, even if the author marks a rule as !important. This can be helpful for situations in which the user wants to increase the font sizes on all web pages he/she uses. 

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
