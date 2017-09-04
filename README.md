<img src="https://devmounta.in/img/logowhiteblue.png" width="250" align="right">

# Project Summary

In this project we'll create a basic Angular application from scratch. Getting used to structuring your Angular application is an important skill to get right. Many times as beginners the hardest part about Angular is figuring out where to put stuff. Hopefully this project will start you on the right path so you can correctly structure all your Angular projects in the future.

## Setup

* Fork and clone this repository.
* Open the project directory in your coding IDE.

## Step 1

### Summary

In this step, we'll create the skeleton of our HTML. This includes an `index.html`, `styles.css`, and a `js` folder.

### Instructions

* Create an `index.html` file.
  * Be sure to include a `DOCTYPE` tag at the top.
  * Be sure to include a `html` tag.
  * Be sure to include a `head` and `title` tag.
  * Be sure to include a `body` tag.
* Add a `paragraph` element to the html that says 'Woo'.
* Create a `styles.css` file.
  * Add css that changes the font color of the `paragraph` element to `red`.
* Link `styles.css` in your `index.html` file.
  * Once you have confirmed your `styles.css` is linked in your `index.html` file, remove the `paragraph` element from `index.html` and the styles from `styles.css`.

### Solution

<details>

<summary> <code> index.html </code> </summary>

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My first angular app!</title>

    <link rel="stylesheet" href="./styles.css">
  </head>

  <body>
    
  </body>
</html>
```

</details>

## Step 2

### Summary

In this step, we'll turn our plain web application into an Angular application. We'll do this by acquiring angular's CDN, specifying our application's name, and specifying our main controller's name.

### Instructions

* Open a browser window and navigate to <a href="https://angularjs.org/">Angular JS</a>
* Click on the download button and then click on `DOWNLOAD ANGULARJS`.
* Click on `1.2.x ( legacy )` and then copy the `CDN` link.
* Open `index.html` and add a `script` tag that links to the Angular CDN just before the closing `body` tag.
* Add a `ng-app` attribute to the `html` tag. Let's call our Angular application `"friendsList"`.
* Add a `ng-controller` attribute to the `body` tag. Let's call our Angular controller `"mainCtrl"`.

### Solution

<details>

<summary> <code> index.html </code> </summary>

```html
<!DOCTYPE html>
<html ng-app="friendsList">
  <head>
    <title>My first angular app!</title>

    <link rel="stylesheet" href="./styles.css">
  </head>

  <body ng-controller="mainCtrl">

    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.32/angular.min.js" />
  </body>
</html>
```

</details>

## Step 3

### Summary

In this step, we'll create the javascript file that creates our Angular application.

### Instructions

* Create a file called `app.js` in `js/`.
* Open `js/app.js`.
* Initialize an Angular application called `"friendsList"`.
* Include `js/app.js` in the `index.html` file.
  * The order is imperative here. Include `js/app.js` just below the Angular CDN.

### Solution

<details>

<summary> <code> js/app.js </code> </summary>

```js
angular.module("friendsList", []);
```

</details>

<details>

<summary> <code> index.html </code> </summary>

```html
<!DOCTYPE html>
<html ng-app="friendsList">
  <head>
    <title>My first angular app!</title>

    <link rel="stylesheet" href="./styles.css">
  </head>

  <body ng-controller="mainCtrl">

    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.32/angular.min.js" />
    <script src="./js/app.js" />
  </body>
</html>
```

</details>