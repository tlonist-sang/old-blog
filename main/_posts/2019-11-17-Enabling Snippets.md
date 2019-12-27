---
layout: post
title:  "Enabling VS code snippets for markdown"
date:   2019-11-17
comments: true
tags: Micellaneous
navigation: True
cover: assets/images/bear.jpg
---


[link_for_enabling_snippets] (https://github.com/Microsoft/vscode/issues/26108)

#### Quick tip for enabling snippets for Markdown

I've been trying to add VS code snippet functions for many times, and the link above was my savior. It is very simple.

1.  Press Shift + CMD + P
2.  Go to Preferences : Configure Language Specific Settings
3.  Choose Markdown
4.  Add the part with __"[markdown]"__

```json
{
    "java.errors.incompleteClasspath.severity": "ignore",
    "C_Cpp.updateChannel": "Insiders",
    "editor.suggestSelection": "first",
    "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
    "window.zoomLevel": 0,
    "workbench.tree.indent": 20,
    "[markdown]": {
        "editor.quickSuggestions": true
    }
}
```

#### The snippet I added

Below is what I added. It makes an image clickable and show its original size. 
This is handy when a figure is not so visible from the html :)

```json
	"Clickable image":{
		"prefix": "imglink",
		"body": [
			"[![img]({{ \"/assets/images/$1\"|absolute_url}})]({{ \"/assets/images/$1\"|absolute_url}})",
			"$2"
		],
		"description": "generate clickable image template"
	},
	"Java Code":{
		"prefix":"javac",
		"body":[
			"```java\n$1\n```"
		],
		"description": "get java code"
	}
```
