+++
author = "andy winarko"
title = "Useful git Command --amend"
description = ""
tags = [
    "git",
]
date = "2019-02-20"
categories = [
    "git",
]
+++

Git udah pasti jadi tools sehari-hari yang dipakai software developer, salah satu command git basic yang sering dipakai adalah  `git commit`.

nah problem yang muncul kalo pake `git commit` biasanya kayak gini,

* ***git commit gua messagenya salah, gantinya gmn ya ?***

* ***eh file gua ada 1 yang gak ke commit, gua bikin commit baru aja ya?***

![image](/img/wait.jpg)

Nah di case-case ini kita bisa pakai option `--amend`

## Case 1

Udah selesai bikin fitur, terus kita `git commit`, nah baru sadar kalau commit messagenya typo. 

disini kita bisa pakai `git commit --amend`

```
git commit --amend -m "New Commit Messages"
```

## Case 2

Udah selesai `git commit`, seletah di cek lagi ada 1 atau beberapa file yang gak ikut ke commit.

sebenernya gak masalah juga sih kalo mau bikin commit baru untuk file yang tadi gak kebawa. tapi biar `git log` nya lebih clean, jadi di case ini kita tambahin filenya ke commit yang udah jadi.

```
git add bublesort.go
git commit --amend --no-edit
```

`--no-edit` artinya commit messagenya gak diganti, atau tetep pakai message yang sebelumnya aja.

---
Sekarang kita udah tau konsep `amending commits`, untuk explore lanjutan, bisa lihat disini 

https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things
