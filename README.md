# Building an Elegant “Gratitude Log” Landing Page With Bulma

*avril 2018*


In this tutorial I am going to run through the process of creating an elegant *Gratitude Log* landing page as designed in a [previous tutorial by Tomas Laurinavicius](https://webdesign.tutsplus.com/tutorials/design-an-elegant-gratitude-log-landing-page-with-photoshop--cms-22787).

To build this landing page, we will use a few tools and medias :

* [Bulma](https://bulma.io)
* [Normalize.css](http://necolas.github.io/normalize.css/)
* [Chillin' in the sun]()
* [PT Serif]()
* [Playfair Display]()
* [Source Sans Pro]()
* [User Inter Faces]()

You can notice that we use the same tools as Thomas in the building of the design.

I would like to learn a new framework : [Bulma](https://bulma.io). 

## Why Bulma and not Bootstrap ?

I've already build some websites with [Bootstrap](http://getbootstrap.com). I really enjoy playing with this CSS Framework. It's friendly, the documentation is great, they're a lot of tutoriel, it's responsive, it's evolving, etc... But. I wanted to learn a new framework. Just to discover a new tool and new techs. And I have no doubt it will improve my CSS skills. 

### Is Bulma different from Bootstrap ?

Short answer : Yes ! Long answer : [see here :-) ](https://bulma.io/alternative-to-bootstrap/)

## File and Folder Structure

We will keep the structure really simple. You will see that we only need a few of JS. So, go ahead and create your folders :

* css/ 
	- grtldStyle.css
* img/
	- 128-2.jpg
	- 128-3.jpg
	- 128-4.jpg
	- 128-5.jpg
	- 128.jpg
	- summerTime.jpg
* index.html

## Install Bulma

I will install Bulma using `npm`.

So first, I've to initiate npm : 

```shell
	npm init
```

After following the instruction, you will have a new file in your folder : package.json.
Now, I can install bulma : 

```shell
	npm install bulma
	npm notice created a lockfile as package-lock.json. You should commit this file.
	+ bulma@0.7.0
	added 1 package from 1 contributor in 2.019s
```

Now, you have a new file and a new folder :
* node_modules/
* package-lock.json

In the `node_modules`, there is only one folder for *Bulma*
Open this folder up and you will see something similar to the following:

## Install normalize

```shell
	npm install normalize.css
```

Back in the day it was Eric Meyer’s css reset, but now you should really be using normalize.css It takes out any of the discrepancies between browser’s default settings. Making all of the default styles the same.

We will need one icon, so we will use [Font Awesome](http://fontawesome.com/) in our project, so do not forget to include it : 
```html
	<script defer src="https://use.fontawesome.com/releases/v5.0.7/js/all.js"></script>
```


## Let's begging to code

Open up index.html and enter the following base HTML:

```html
	<!DOCTYPE html>
	<html>
	  <head>
	    <meta charset="utf-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1">
	    <title>Gratitude Log</title>
	    <link rel="stylesheet" href="node_modules/normalize.css/normalize.css">
	    <link rel="stylesheet" href="node_modules/bulma/css/bulma.min.css">
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

The <head> section contains the necessary viewport tag so our media queries work correctly. Next, we give the page a title and include a <link> tag for the various Google fonts we want to use. The fonts here are based on those used in the design by Thomas. The next line may seem strange because we haven't created a style.css file yet, but generating that file will be handled by our Sass compiler. Lastly, we include Modernizr.

The <body> element contains four other elements to hold each of the bands which appear on the design. I have applied some descriptive classes to the <section> elements so we can clearly see what they will be used for.

### Step 2 :

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

