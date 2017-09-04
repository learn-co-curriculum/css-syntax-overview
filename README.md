# Intro To CSS

Now that we understand the goal of CSS, let's talk about actually using CSS to change the look of our websites. 

CSS is broken down into two sections, first we have to tell the browser _what_ we want to change. Then we tell the browser _how_ we want that thing changed. Let's look at an example:


<iframe height='265' scrolling='no' title='CSS Intro' src='//codepen.io/joemburgess/embed/awpedE/?height=265&theme-id=0&default-tab=html,result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/joemburgess/pen/awpedE/'>CSS Intro</a> by Joe Burgess (<a href='https://codepen.io/joemburgess'>@joemburgess</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

Taking a look at the CSS tab you should see this text:

```css
body {
  color: red;
}
```

If we break that down a bit the word `body` is telling CSS _what_ to change. The `color: red;` is telling CSS _how_ to change that. In addition to the how and the what, we have some syntax requirements as well. Let's add in another change to the `body`. Change the code in the CSS tab to say:

```css
body {
  color: red;
  font-weight: bold;
}
```

You'll notice all the font is bold now. Every line describing how things change need to be ended with a `;`. You wrap all of the ways you want the thing to change with `{` and `}` characters.

### Selecting elements
What if we wanted only our header to be red, but the rest of the body to be black? All you have to do is change the _what_ in our CSS. So, we need to change the `body` to `h1`. Modify your CSS to look like this:

```css
h1 {
  color: red;
  font-weight: bold;
}
```

The header should be red now, but the rest of the body is black and no longer bolded. To get our body bolded we simply need two different _what_ blocks. Something like this:

```css
h1 {
  color: red;
}

p {
  font-weight: bold;
}
```

Now we are bolding all of the paragraph tags. Everything seems great. The designer comes over and says "Hey, could you make the first paragraph a bit larger?" You think for a second and google how to change the font size. A quick google says `font-size: 15pt` will make your font larger. Now you know the _how_, but we don't have any way of distinguishing one `p` tag from the other.

Thankfully, this problem is solved with the `id` attribute. You can add an `id` attribute to any tag which will then allow you to identify that specific tag. To do this re-write the code in the HTML tag to look like this:

```html
<html>
  <head>
  </head>
  <body>
     <h1>Profile</h1>
    <p id="first">
    Hello, my name is Joe Burgess. 
<br>
     I'm a teacher at The Flatiron School.
    </p>
  <p>
  I've been teaching at The Flatiron School for four years. Programming was an early passion of mine and I started coding on TI-83 calculators in BASIC when I was in middle school. 
  </p>
  </body>
</html>
```

You'll notice that first `p` tag has `id="first"`. Now to access that we write our CSS like this:

```css
h1 {
  color: red;
}

p {
  font-weight: bold;
}

#first {
  font-size: 15pt;
}
```

`id` tags are identified by prefixing the `id` with a `#` character. Your final CodePen should look like this:

<iframe height='265' scrolling='no' title='completed-css' src='//codepen.io/joemburgess/embed/MoJNvo/?height=265&theme-id=0&default-tab=html,result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/joemburgess/pen/MoJNvo/'>completed-css</a> by Joe Burgess (<a href='https://codepen.io/joemburgess'>@joemburgess</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

In the next lesson we will go deeper into the ways you can select elements. There are a ton!
