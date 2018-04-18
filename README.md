# Tutorial : Building a “Gratitude Log” Landing Page With [Bulma](https://bulma.io)

*April 2018*

In this tutorial I am going to run through the process of creating a *Gratitude Log* landing page as designed [by Tomas Laurinavicius.](https://webdesign.tutsplus.com/tutorials/design-an-elegant-gratitude-log-landing-page-with-photoshop--cms-22787).

To build this page, we will use :

* Tools : 
	* [Bulma](https://bulma.io)
	* [Normalize.css](http://necolas.github.io/normalize.css/)
* Pictures : 
	* [Chillin' in the sun](https://skitterphoto.com/photos/895/chilling-in-the-park)
	* Avatars from [User Inter Faces](http://uifaces.com)
* Fonts: 
	* [PT Serif](https://www.fontsquirrel.com/fonts/pt-serif)
	* [Playfair Display](https://www.fontsquirrel.com/fonts/playfair-display)
	* [Source Sans Pro](https://www.fontsquirrel.com/fonts/source-sans-pro)

## What's [Bulma](https://bulma.io) and why use it ?

Bulma is an open source CSS framework based on Flexbox and created by [Jeremy Thomas](https://jgthms.com/). I wanted to learn a new framework,  discover a new tool and I have no doubt it will improve my CSS skills. Bulma is an alternative to Bootstrap, Jeremy explain how [here](https://bulma.io/alternative-to-bootstrap/).

## Install [Bulma](https://bulma.io)

First, let's install Bulma. There are several ways to use Bulma. Here, I decided to install the Bulma's package with `npm` :
1. Open your terminal
1. Create a new folder
1. Initiate `npm`
1. Install `bulma`


```shell
	~/Web  mkdir Grttd
 	~/Web  cd Grttd
 	~/Web/Grttd  npm init
	~/Web/Grttd  npm install bulma
	npm notice created a lockfile as package-lock.json. You should commit this file.
	+ bulma@0.7.0
	added 1 package from 1 contributor in 2.019s
	 ~/Web/Grttd  ls
node_modules      package-lock.json package.json
```

## Install [normalize.css](https://necolas.github.io/normalize.css/)

```shell
	npm install normalize.css
```

`Normalize.css is a small CSS file that provides better cross-browser consistency in the default styling of HTML elements. It’s a modern, HTML5-ready, alternative to the traditional CSS reset.`

## Files and Folder structure

So far, here are the files and the folder structure :
* css/
	- grttdStyle.css
* img/
	- 128-2.jpg
	- 128-3.jpg
	- 128-4.jpg
	- 128-5.jpg
	- summerTime.jpg
* node_modules/
	- bulma/
	- normalize.css/
* index.html


Create the folders needed and already add the images.

## Let's dive into the code

Open up `index.html` and enter the following base HTML:

```html
	<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Gratitude Log</title>
  <link rel="stylesheet" href="node_modules/normalize.css/normalize.css">
  <link rel="stylesheet" href="node_modules/bulma/css/bulma.min.css">
  <script defer src="https://use.fontawesome.com/releases/v5.0.7/js/all.js"></script>
</head>
<body>
  <section class="section">
    <div class="container">
      <h1 class="title">
        Gratitude Log
      </h1>
      <p class="subtitle">
        My first website with <strong>Bulma</strong>!
      </p>
    </div>
  </section>
</body>
</html>
```

We have our first bit of code! Let's break it down. 

This code is based on starter template from Bulma. Really clean and short. The <head> section contains the necessary viewport tag so our media queries work correctly. I've linked the css files from the nodes folders and add a script to be able to use the icons from Font Awesome. 

The <body> element contains is almost empty for the moment. I will follow the process of Thomas for the rest of the page.

## Building the header area :

We want something approaching this :
![Header Area](/PSD/headerArea.png)

``` html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Gratitude Log</title>
    <link rel="stylesheet" href="node_modules/normalize.css/normalize.css">
    <link rel="stylesheet" href="node_modules/bulma/css/bulma.min.css">
    <link rel="stylesheet" href="css/grttdStyle.css">
    <script defer src="https://use.fontawesome.com/releases/v5.0.7/js/all.js"></script>
</head>
<body>
  	<section class="hero is-info is-large">
		<div class="hero-head">
		    <nav class="navbar">
		      <div class="container">
		        <div class="navbar-brand">
		          <a class="navbar-item">
		            <h1>Grttd</h1>
		          </a>
		          <span class="navbar-burger burger" data-target="navbarMenuHeroB">
		            <span></span>
		            <span></span>
		            <span></span>
		          </span>
		        </div>
		        <div id="navbarMenuHeroB" class="navbar-menu">
		          <div class="navbar-end">
		            <a class="navbar-item is-active">
		              Home
		            </a>
		            <a class="navbar-item">
		              Get involved
		            </a>
		            <a class="navbar-item">
		              Get inspired
		            </a>
		            <a class="navbar-item">
		              Stories
		            </a>
		            <a class="navbar-item">
		              Contact
		            </a>
		            <span class="navbar-item">
		              <a class="button is-info is-inverted">
		                <span class="icon">
		                  <i class="fas fa-sign-in-alt"></i>
		                </span>
		                <span>Sign up</span>
		              </a>
		            </span>
		          </div>
		        </div>
		      </div>
		    </nav>
		  </div>

		<div class="hero-body">
		    <div class="container has-text-centered">
		      <p class="title">
		        Being Grateful Makes<br> You More Successful
		      </p>
		      <p class="subtitle">
		        Create Gratitude Log. Be happier. Change your life.
		      </p>
		      <a class="button is-info is-inverted">
		        <span>Start Living</span>
		        <span class="icon">
		            <i class="fas fa-arrow-right"></i>
		        </span>
		       </a>
		    </div>
  		</div>
	</section>
</body>
</html>
```

``` css
/*! Generated by Font Squirrel (https://www.fontsquirrel.com) on April 16, 2018 */



@font-face {
    font-family: 'source_sans_problack';
    src: url('../fonts/sourcesanspro-black-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-black-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_problack_italic';
    src: url('../fonts/sourcesanspro-blackit-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-blackit-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_probold';
    src: url('../fonts/sourcesanspro-bold-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-bold-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_probold_italic';
    src: url('../fonts/sourcesanspro-boldit-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-boldit-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_proextralight';
    src: url('../fonts/sourcesanspro-extralight-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-extralight-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_proXLtIt';
    src: url('../fonts/sourcesanspro-extralightit-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-extralightit-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_proitalic';
    src: url('../fonts/sourcesanspro-it-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-it-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_prolight';
    src: url('../fonts/sourcesanspro-light-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-light-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_prolight_italic';
    src: url('../fonts/sourcesanspro-lightit-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-lightit-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_proregular';
    src: url('../fonts/sourcesanspro-regular-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-regular-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_prosemibold';
    src: url('../fonts/sourcesanspro-semibold-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-semibold-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'source_sans_proSBdIt';
    src: url('../fonts/sourcesanspro-semiboldit-webfont.woff2') format('woff2'),
         url('../fonts/sourcesanspro-semiboldit-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}

/*! Generated by Font Squirrel (https://www.fontsquirrel.com) on April 16, 2018 */



@font-face {
    font-family: 'playfair_displayblack';
    src: url('../fonts/playfairdisplay-black-webfont.woff2') format('woff2'),
         url('../fonts/playfairdisplay-black-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'playfair_displayblack_italic';
    src: url('../fonts/playfairdisplay-blackitalic-webfont.woff2') format('woff2'),
         url('../fonts/playfairdisplay-blackitalic-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'playfair_displayitalic';
    src: url('../fonts/playfairdisplay-italic-webfont.woff2') format('woff2'),
         url('../fonts/playfairdisplay-italic-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}




@font-face {
    font-family: 'playfair_displayregular';
    src: url('../fonts/playfairdisplay-regular-webfont.woff2') format('woff2'),
         url('../fonts/playfairdisplay-regular-webfont.woff') format('woff');
    font-weight: normal;
    font-style: normal;

}
body{
	color: #0e0e0e;
}
h1{
	font-family: 'playfair_displayblack_italic', serif;
	font-size: 1.6em;
	text-transform: none;
}
.hero{
	position: relative;
}
.hero-head{
	position: absolute;
	background-color: white;
	align-self: center;
	top: 50px;
	width: 90%;
}
.hero.is-info{
	background-color: white;
	color: #0e0e0e;
}
.hero.is-info a.navbar-item, .button.is-info.is-inverted{
	font-family: 'source_sans_proregular', sans-serif;
	text-transform: uppercase;
	color: #0e0e0e;
}
.hero.is-info a.navbar-item.is-active{
	background: none;
	border-bottom: 1px solid #0e0e0e;
}
.hero.is-info a.navbar-item:hover{
	background: none;
	border-bottom: 1px solid #0e0e0e;
}
.hero-body{
	background:url(../img/summerTime.jpg) no-repeat center center;
	background-size: cover;
}

.title{
	font-family: 'source_sans_problack', sans-serif;
	font-size: 4em;
}
.subtitle{
	font-family: 'playfair_displayitalic', serif;
}
.button{
	border-radius: 0;
	padding: 1em 2em;
}

@media screen and (max-width: 768px){
	.hero-head{
		position: relative;
		align-self: center;
		top: 0;
		width: 100%;
	}
}

```

