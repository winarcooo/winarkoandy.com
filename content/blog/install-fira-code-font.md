+++
author = "andy winarko"
title = "Install Fira-Code font"
description = ""
tags = [
    "font",
    "ligature",
]
date = "2019-02-20"
categories = [
    "font",
]
+++

Kenapa Fira Code ? 😕

> Programmers use a lot of symbols, often encoded with several characters. For the human brain, sequences like `->`, `<=` or `:=` are single logical tokens, even if they take two or three characters on the screen. Your eye spends a non-zero amount of energy to scan, parse and join multiple characters into a single logical one. Ideally, all programming languages should be designed with full-fledged Unicode symbols for operators, but that’s not the case yet.

Intinya font ini ada ligature-nya buat ubah beberapa symbol yang sering kita pakai jadi lebih enak dilihat mata 👀.

---


![image](/img/all_ligatures.png)

Contohnya,

*Javascript*
![image](/img/javascript.png)

*Go*
![image](/img/go.png)

**1. Install Fira Code**

```bash
brew tap caskroom/fonts
brew cask install font-fira-code
```

Udah itu aja, dan jangan lupa aktifin fitur ✅ `enable/use ligatures` di terminal atau editor yang dipakai.


### Terminal support

| Works              | Doesn’t work       |
| ------------------ | ------------------ |
| **Butterfly**      | **Alacritty**      |
| **Hyper.app**      | **cmd.exe**        |
| **iTerm 2** ([3.1+](https://gitlab.com/gnachman/iterm2/issues/3568#note_13118332)) | **Cmder** |
| **Kitty**          | **ConEmu**         |
| **Konsole**        | **GNOME Terminal** | 
| **mintty** (partial support [2.8.3+](https://github.com/mintty/mintty/issues/601))| **mate-terminal** |
| **QTerminal**      | **PuTTY**          |
| **Terminal.app**   | **rxvt**           |
| **Termux**         | **ZOC** (Windows)  |
| **Token2Shell/MD** | **gtkterm, guake, LXTerminal, sakura, Terminator, xfce4-terminal,** and other libvte-based terminals ([bug report](https://bugzilla.gnome.org/show_bug.cgi?id=584160)) |
| **upterm**         |
| **ZOC** (macOS)    |

### Editor support

| Works | Doesn’t work   |
| ----- | -------------- |
| **Abricotine** | **Arduino IDE** |
| **Android Studio** (2.3+, [instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) | **Adobe Dreamweaver** |
| **Anjuta** (unless at the EOF) | **Delphi IDE** |
| **AppCode** (2016.2+, [instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) | **Eclipse** (Win, [vote here](https://bugs.eclipse.org/bugs/show_bug.cgi?id=398656)) |
| **Atom** 1.1 or newer ([instructions](https://github.com/tonsky/FiraCode/wiki/Atom-instructions)) | Standalone **Emacs** ([workaround](https://github.com/tonsky/FiraCode/wiki/Emacs-instructions)) |
| **BBEdit/TextWrangler** (v. 11 only, [instructions](https://github.com/tonsky/FiraCode/wiki/BBEdit-instructions)) | **gVim** (Windows [workaround](https://github.com/tonsky/FiraCode/issues/462)) |
| **Brackets** (with [this plugin](https://github.com/polo2ro/firacode-in-brackets)) | **IDLE** |
| **Chocolat** | **KDevelop 4** |
| **CLion** (2016.2+, [instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) | **Monkey Studio IDE** |
| **Cloud9** ([instructions](https://github.com/tonsky/FiraCode/wiki/Cloud9-Instructions)) |  |
| **Coda 2** |  |
| **CodeLite** |  |
| **Eclipse** (Mac 4.7+, Linux) |  |
| **elementary Code** |  |
| **Geany** |
| **gEdit / Pluma** |
| **GNOME Builder** |
| **GoormIDE** ([instructions](https://github.com/tonsky/FiraCode/wiki/GoormIDE-Instructions)) |
| **IntelliJ IDEA** (2016.2+, [instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) |
| **Kate, KWrite** |
| **Komodo** |
| **Leafpad** |
| **LibreOffice** |
| **LightTable** ([instructions](https://github.com/tonsky/FiraCode/wiki/LightTable-instructions)) |
| **LINQPad** |
| **MacVim** 7.4 or newer ([instructions](https://github.com/tonsky/FiraCode/wiki/MacVim-instructions)) |
| **Mancy** |
| **Meld** |
| **Mousepad** |
| **NeoVim-gtk** |
| **NetBeans** |
| **Notepad** (Win) |
| **Notepad++** (with a [workaround](https://github.com/notepad-plus-plus/notepad-plus-plus/issues/2287#issuecomment-256638098))  |
| **PhpStorm** (2016.2+, [instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) |
| **PyCharm** (2016.2+, [instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) |
| **QtCreator** |
| **Rider** |
| **RStudio** ([instructions](https://github.com/tonsky/FiraCode/wiki/RStudio-instructions)) |
| **RubyMine** (2016.2+, [instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) |
| **Scratch** |
| **Scribus** (1.5.3+) |
| **SublimeText** (3146+) |
| **Spyder IDE** (only with Qt5) |
| **SuperCollider 3** |
| **TextAdept** (Linux, Mac) |
| **TextEdit** |
| **TextMate 2** |
| **VimR** ([instructions](https://github.com/qvacua/vimr/wiki#ligatures)) |
| **Visual Studio 2015** |
| **Visual Studio 2017** ([instructions](https://github.com/tonsky/FiraCode/wiki/Visual-Studio-2017-Instructions)) |
| **Visual Studio Code** ([instructions](https://github.com/tonsky/FiraCode/wiki/VS-Code-Instructions)) |
| **WebStorm** (2016.2+, [instructions](https://github.com/tonsky/FiraCode/wiki/Intellij-products-instructions)) |
| **Xamarin Studio/Monodevelop** |
| **Xcode** (8.0+, otherwise [with plugin](https://github.com/robertvojta/LigatureXcodePlugin)) |
| Probably work: **Smultron, Vico** | Under question: **Code::Blocks IDE** |

[*github.com/tonsky/FiraCode*](https://github.com/tonsky/FiraCode)
