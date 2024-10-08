## STYLESHEET LINK

When styling in your stylesheet, don't forget to link your stylesheet in `index.html` at head element.
```html
<link rel="stylesheet" type="text/css" href="style.css">
```

## MARGIN SET

After you've linked it, now we're gonna set the font, and margin of body and container class. 

Body margin and padding will be set to 0 so there will be no white space left at the navbar.

at your stylesheet, add:
```css
body {
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
margin: 0;
padding: 0;
}      

.container {
    max-width: 1170px;
    margin: 0 auto; /* it will set the right and left margin follow the width */
}
```

## FLOAT LEFT AND RIGHT

Margin has been set, now we will make the structure become:


    +-------------------------------------------------+                         +-------------------------------------------------+
    |HOME                                             |                         |  HOME                  SKILL EXPERIENCE CONTACT |
    |SKILL EXPERIENCE CONTACT                         |                         |                                                 |
    |                                                 |                         |                                                 |
    |                                                 |         Become          |                                                 |
    |                                                 |         =====>          |                                                 |
    |                                                 |                         |                                                 |
    |                                                 |                         |                                                 |
    |                                                 |                         |                                                 |
    |                                                 |                         |                                                 |
    +-------------------------------------------------+                         +-------------------------------------------------+ 

We can simply set the `left-nav` to be `float: left` and the `right-nav` to be `float: right`.

`float` property will make the element floated to a set direction like what we've planned.

So we're gonna add in stylesheet:
```css
.right-nav {
    float: right;
    margin-right: -25px;
}
.left-nav {
    float: left;
}            
```          
After you add that, see the difference it makes.

## NAVBAR COLOR

Now we're gonna set the color to make it more colorfull. 

we can select the `<nav>` and set the background color you like and set the height of your navbar.

Because I like blue color, so we're gonna set it to blue and for the height we'll set it to `65px`.
```css
nav {
    height: 65px;
    background-color: #528aae;
}
```

The navbar color has been changed, but the text hasn't changed, so we're gonna set it to white and make it center so

we can read it more clearly.
```css
.right-nav a, .left-nav a{          /* It will change both of em */
    line-height: 65px;
    color: white;
}
```

It is a bit narrow for the right-nav isn't it? let's add some padding!!
```css
.right-nav a{
    line-height: 65px;
    padding: 0 25px;
    color: white;
}
.left-nav a{
    line-height: 65px;
    padding: 0 25px;
    color: white;
}
```

now it looked like a navbar right?? but it is still tooooooo plain, let's add the makeup more ^_^

## MOREEEEE
do you see some underlined text in the `<a>` tags? it bothers no? so we're gonna make it disappear!!

we're gonna set * text-decoration: none * so the decoration like that underline will be gone for all `<a>` tags.
```css
a {
    text-decoration: none;
}
```

now the underline gone, we'll add some hover effect at the menu to make it cooler.

## HOVERED COLOR

To make a change to an element when hovered, we've learned it before in 7_css_selector. what change wil be made?

Here we'll set the color of the box will be darker when hovered for both left and right nav, so the code is:
```css
.right-nav :hover, .left-nav :hover{
    color: #1975af;
}
```

But with those code, it just changed the text color, how if we want to change the text box color?

we must set the `<a>` tags of right and left nav display to block, so it will become block-like structure.
```css
.right-nav a {
    line-height: 65px;
    padding: 0 25px;
    display: block;
    color: white;
    float: left; /* to make it horizontal align (see the difference when there's no float in block) */
}
.left-nav a {
    line-height: 65px;
    display: block;
    color: white;
}
```

And after that, if before we changed the color of right/left-nav, now we're gonna change it to background-color so the whole box will be changed.

before: 
```css
.right-nav :hover, .left-nav :hover{
    color: #1975af;
}
```

after: 
```css
.right-nav :hover, .left-nav :hover{
    background-color: #1975af;
}
```

and make it smoother with transition.
```css
.right-nav :hover, .left-nav :hover{
    background-color: #1975af;
    transition: 0.5s; /* it will give some time to the targeted effect */
}
.right-nav a {
    line-height: 65px;
    padding: 0 25px;
    display: block;
    color: white;
    float: left;
    transition: 0.5s; /* it will give some time to the targeted effect */
}
.left-nav a {
    line-height: 65px;
    display: block;
    color: white;
    transition: 0.5s; /* it will give some time to the targeted effect */
}
```

YEAY you've make your navbar now, next we're gonna go to to fill a little bit of content in your web profile.
