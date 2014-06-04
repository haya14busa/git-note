Atom
====
- [Slide](https://www.dropbox.com/s/utaud80bk5egse3/Atom%20%E2%80%93%20GitHub%20Kaigi_jp.pdf)

Profile: @nathansobo
--------------------
- Nathan Sobo (@nathansobo)
  - [Github: @nathansobo](https://github.com/nathansobo)
  - [Twitter: @nathansobo](https://twitter.com/nathansobo)

Atom
----
- Started Summer 2001
- Beta February 2014
- Open Source May 2014

> "Every good work of software starts by scratching a developer's personal itch."

> - Eric Raymond

- Vim: How much I Can think
- Sublime: 機能スゴイ

最も影響があるエディタ: Emacs & Textmate
----------------------------------------

### Emacs:
- extendability
- API
- Open
- freshmanで初めて使ってびっくり
  - 今までのデスクトップアプリと全く違う

### Textmate
- DHHのRails Videoデモ
- 使い始めてすぐ使える
- Not programmable

### -> 自分で作ってみたい
- Emacs
  - Deeply Programmable
  - Unapproachable
  - Configuration on Day 1
- Textmate
  - Approchable
  - Batteries Included
    - (最初から必要な機能が備わっている)
  - Limited Possibilities

### Emacs
- CoreとUser Extensions(Emacs Lisp)の境界がほぼない

最初にnative層を開発:

- cross platform
- performance
- script language
- Atomではそもそも言語から作る必要なかった

Application platform -> **Web browser**

- TextMateと同じSimpleなインターフェース
- あくまでstart point

### Graphic Framework
- consoleより成熟されたHTML5,CSS3


Demo
----
- Developers Console使える
- less(css)でマークダウンのheader,cursor,などなどがスタイリングできる

Node, Chromium, V8でいままでのJavaScriptで出来なかったこともできるように!(IOなど)

Modularity < Node

3 min develop atom package
--------------------------
- Generatorある
- `package.json`
- npm moduleが使えるので便利

```coffee
module.exports =
  activate: ->
    atom.workspaceView.command 'ascii-art:convert', => @convert()

  convert: ->
    editor = atom.workspace.getActiveEditor()

    figlet = require 'figlet'

    figlet editor.getSelectedText(), font: "Larry 3D 2", (error, asciiArt) ->
    ...
```

How Can You Get Involved?
-------------------------
- つかってかゆいところ探す
- community, 人を重視(GitHub)

Atom
----
- [Atom](https://atom.io/)
- [atom/atom](https://github.com/atom/atom)

KeymapはCSS basd
