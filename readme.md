
```sh
$ mkdir love_song
$ cd love_song
$ git init
$ touch lyrics.txt
```

```text
---
Love Song (Working Title)
By Milt Gabler

---
```

```sh
$ git add lyrics.txt
$ git commit -m "Initial commit"
```

```text
---
Love Song (Working Title)
By Milt Gabler

"L" is for the way you look at me

---
```

```sh
$ git add lyrics.txt
$ git commit -m "Solid first line"
```

```sh
$ git branch try-romance
$ git checkout try-romance
```

```text
---
Love Song (Working Title)
By Milt Gabler

"L" is for the way you look at me

"O" is for the only one I see

---
```

```sh
$ git add lyrics.txt
$ git commit -m "Wondering if I can spin this as a love song instead?"
```

```sh
$ git checkout master
```

```text
---
Love Song (Working Title)
By Milt Gabler

"L" is for the way you look at me

"O" is for ophthalmology

"V" is very extraordinary

---
```

```sh
$ git add lyrics.txt
$ git commit -m "Added blurb about eye doctors being so special"
```

```sh
$ git merge try-romance
```

```text
---
Love Song (Working Title)
By Milt Gabler

"L" is for the way you look at me

"O" is for the only one I see

"V" is very extraordinary

---
```

```sh
$ git add lyrics.txt
$ git commit -m "Going with love song, but keeping the 'V' line."
```

```
$ git branch -d try-romance
```
