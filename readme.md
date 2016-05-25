# Love and Conflict

```sh
$ mkdir love_song
$ cd love_song
$ git init
$ touch index.html
```

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Love Song</h1>
    <p>By Milt Gabler</p>
  </body>
</html>
```

```sh
$ git add index.html
$ git commit -m "Initial commit"
```

```sh
$ git branch wip-lyrics
$ git checkout wip-lyrics
```

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Love Song</h1>
    <p>By Milt Gabler</p>
    <ul>
      <li><dfn>L</dfn> is for the way you look at me.</li>
    </ul>
  </body>
</html>
```

```sh
$ git add index.html
$ git commit -m "Solid first line"
```

```sh
$ git checkout master
$ git merge wip-lyrics
```

```sh
$ git branch wip-css
$ git checkout wip-css
$ touch styles.css
```

```css
body{
  text-align:center;
}
```

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Page</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Love Song</h1>
    <p>By Milt Gabler</p>
    <ul>
      <li><dfn>L</dfn> is for the way you look at me.</li>
    </ul>
  </body>
</html>
```

```sh
$ git add .
$ git commit -m "Added stylesheet"
$ git checkout master
$ git merge wip-css
```

```sh
$ git checkout wip-lyrics
```

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Love Song</title>
  </head>
  <body>
    <h1>Love Song</h1>
    <p>By Milt Gabler</p>
    <ul>
      <li><dfn>L</dfn> is for the way you look at me.</li>
    </ul>
  </body>
</html>
```

```sh
$ git add .
$ git commit -m "Fixed title"
```

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Love Song</title>
  </head>
  <body>
    <h1>Love Song</h1>
    <p>By Milt Gabler</p>
    <ul>
      <li><dfn>L</dfn> is for the way you look at me.</li>
      <li><dfn>O</dfn> is for the only one I see.</li>
    </ul>
  </body>
</html>
```

```sh
$ git add .
$ git commit -m "Added second line"
$ git checkout master
$ git merge wip-lyrics
```

## Merge conflict 

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Love Song</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Love Song</h1>
    <p>By Milt Gabler</p>
    <ul>
      <li><dfn>L</dfn> is for the way you look at me.</li>
      <li><dfn>O</dfn> is for the only one I see.</li>
    </ul>
  </body>
</html>
```

```sh
$ git add .
$ git commit -m "Merging CSS and changes to lyrics"
```

```sh
$ git checkout wip-lyrics
```

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Love Song</title>
  </head>
  <body>
    <h1>Love Song</h1>
    <p>By Milt Gabler</p>
    <ul>
      <li><dfn>L</dfn> is for the way you look at me.</li>
      <li><dfn>O</dfn> is for the only one I see.</li>
      <li><dfn>V</dfn> is very very extraordinary.</li>
      <li><dfn>E</dfn> is even more than anyone that you adore can.</li>
    </ul>
  </body>
</html>
```

```sh
$ git add .
$ git commit -m "Finished first verse"
```

```sh
$ git checkout wip-css
```

```css
body{
  text-align:center;
  font-family:"Comic Sans MS";
}
```

```sh
$ git add .
$ git commit -m "Added some very Web2.0 fonts"
```

```sh
$ git checkout master
$ git merge wip-css
$ git merge wip-lyrics
$ git branch -d wip-css
$ git branch -d wip-lyrics
```
