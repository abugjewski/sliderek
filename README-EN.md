# Sliderek
A little library for implementing a slider into your website.
*Description also available in [Polish](https://github.com/abugjewski/sliderek/blob/master/README.md)*
- - -
##Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Installation](#installation)
* [How to use](#how-to-use)
* [Inspiration](#inspiration)
* [Contact](#contact)
- - -
##General info
Sliderek allows the user to use a simple slider with images and their description (if needed) on his/hers website. By default, the project was simply to be just it - a slider. However it was modified to make it easy to include it in (at least in theory) any website. Without a doubt there are thing to improve on but it should ensure basic functionalities.
- - -
##Technologies
* HTML
* CSS
* Javascript
- - -
##Installation
After downloading the library you just need to include *sliderek.css* and *sliderek.js* files in your project. The easiest way to do so is to add them in the \<head> tag of your website. The simplest example should look like this:
```html
<head>
    <link rel="stylesheet" href="sliderek/sliderek.css">
    <script src="sliderek/sliderek.js" defer>
</head>
```
##How to use
After you include Sliderek in your website, add *createSliderek()* function in your custom javascript script like this:
```javascript
createSliderek(".box", slides);
```
The first argument of this function refers to the element in which you want to insert the slider. You can refer to it via classname or id. This argument should be of type *String*.
The second argument refers to an array of objects which contains information about each slide. Every such a object can have certain properties:
* **img** - *type String*. Refers to slides image path.
* **title** - *typ String*. Slide title.
* **content** - *typ String*. Slide description.
* **slideFrom** - *typ String*. Determines the side from which the slide will slide in. Values it can take are *top*, *bottom*, *left* and *right*. The default value is *top*.
* **contentFrom** - *typ String*. Determines the side from which the slides title and/or description will enter the slide. Values are the same as in *slideFrom* property. The default value is *top*.
* **contentDelay** - *typ Number*. Defines the delay (in seconds) after which the slide title and/or description will enter the slide.
- - -
##Inspiration
The slider itself was created based on a youtube tutorial from this [link](https://www.youtube.com/watch?v=PDVr7qNytTg).
- - -
##Contact
Project created by [Adrian Bugajewski](https://abugjewski.github.io/portfolio/). If you have questions, suggestions or other things in mind, feel free to contact me!