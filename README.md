
## New Reveal.js Theme

### Brief of Summary
The website is a reveal.js theme that it has different styles from the original reveal.js theme.
This template has a background image, logo image, and specific font

### The difference between the original theme and this theme
- Background image: an image appears in all slides as a background, this template used this background
![](https://raw.githubusercontent.com/shahenazmonia/blog/master/chalkboard%20Background%20Tall.jpg)
- Font: annie get your telescope
- Logo : this template used ![](https://raw.githubusercontent.com/shahenazmonia/blog/master/pepsi-logo-1.png)


### Code Architecture
The entry point is index.html file, this file calls black.css style file
So you can change every style appears in the website from black.css file. Path of the file is css/theme/black.css

##### Change Background Image
Right now inside class ```body``` you can change style that it appears in whole slides, so background image has changed inside.

```js
 body {
  background-repeat:no-repeat;
  background-size: cover;
  background-image: url('./background.jpg');
}
```
* background-image is a link of image
* background-size is a shape of how the image will appear
* background-repeat that means no repeat for the image

##### Change Logo Image

There is ``` body:after``` class, this tag used to add another image on the background image, so you can add logo image inside.
About the change logo placement, you can use ```top, down, left, and right``` then add the distance you want the logo to go away from

```js
body:after {
  content: url('./pepsi-logo-1.png');
position: fixed;
top: '0.5em';
left: '3.5em';
 }
```

##### Change The Font
- Download the required font.
- Add the downloaded font inside theme folder
- Call the font inside black.css file

```js
@font-face{
  font-family: 'Annie Use Your Telescope';
  src: url("./AnnieUseYourTelescope-Regular.ttf");
}
```
OR
- Take an online font link
- Add the link inside ```index.html``` file between link tag


Also font has changed inside ```reveal``` class and every tag related to reveal class like ```.reveal h1,.reveal h2```, etc..

Inside these classes you can change font size, font weight, font type and font color. this style will apply on each slide in a theme

```js
.reveal {
  font-family: 'Annie Use Your Telescope', cursive;
  color: #e0dbd1;
  font-size: 42px;
  font-weight: normal;
}
.reveal h1,
.reveal h2,
.reveal h3,
.reveal h4,
.reveal h5,
.reveal h6 {
  color: #e0dbd1;
  font-family: 'Annie Use Your Telescope', cursive;
    font-weight: 600;
   }
```  
