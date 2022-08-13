
# Learn Basic CSS by Building a Cafe Menu, Completed
> - CSS tells the browser how to display your webpage. You can use CSS to set the color, font, size, and other aspects of HTML elements.
> - In this course, you'll learn CSS by designing a menu page for a cafe webpage.
---

> **Step 1** <br>
As you learned in the last few steps of the Cat Photo App, there is a basic structure needed to start building your web page.<br>
Add the `<!DOCTYPE html>` tag, and an `html` element with a `lang` attribute of `en`.

```html
<!DOCTYPE html>
<html lang="en">
</html>
```
> **Step 2** <br>
Add a `head` element within the `html` element, so you can add a `title` element. The `title` element's text should be `Cafe Menu`.

```html
<!DOCTYPE html>
<html lang="en">
```
```html
    <head>
        <title>Cafe Menu</title>
    </head>
```
```html
</html>
```
> **Step 2** <br>
The `title` is one of several elements that provide extra information not visible on the web page, but it is useful for search engines or how the page gets displayed.<br>
Inside the `head` element, nest a `meta` element with an attribute named `charset` set to the value `utf-8` to tell the browser how to encode characters for the page. Note that `meta` elements are self-closing.

```html
    <head>
        <meta charset="UTF-8">
        <title>Cafe Menu</title>
    </head>
```
> **Step 4** <br>
To prepare to create some actual content, add a `body` element below the `head` element.

```html
    <head>
        <meta charset="UTF-8">
        <title>Cafe Menu</title>
    </head>

    <body>

    </body>
```
> **Step 5** <br>
The name of the cafe is `CAMPER CAFE`. Add an `h1` element within your `body` element. Give it the name of the cafe in capitalized letters to make it stand out.

```html

    <body>
        <h1>CAMPER CAFE</h1>
    </body>
```
> **Step 6** <br>
To let visitors know the cafe was founded in 2020, add a `p` element below the `h1` element with the text `Est. 2020`.

```html
    <body>
        <h1>CAMPER CAFE</h1>
        <p>Est. 2020</p>
    </body>
```
> **Step 7** <br>
Since the `p` element added in the previous step provides supplemental information about the cafe, nest both the `h1` and `p` elements in a `header` element.

```html
    <body>
        <header>
            <h1>CAMPER CAFE</h1>
            <p>Est. 2020</p>
        </header>
    </body>
```
> **Step 8** <br>
It's time to add some menu content. Add a `main` element below the existing `header` element. It will eventually contain pricing information about coffee and desserts offered by the cafe.

```html
    <body>
        <header>
            <h1>CAMPER CAFE</h1>
            <p>Est. 2020</p>
        </header>

        <main>
        
        </main>
    </body>
```
> **Step 9** <br>
There will be two sections on the menu, one for coffees and one for desserts. Add a `section` element within the `main` element so you have a place to put all the coffees available.

```html
        <main>
            <section>
            </section>
        </main>
```
> **Step 10** <br>
Create an `h2` element in the `section` element and give it the text<br> 
`Coffee`.

```html
        <main>
            <section>
                <h2>Coffee</h2>
            </section>
        </main>
```
> **Step 11** <br>
Up until now, you have been limited regarding the presentation and appearance of the content you create. To start taking control, add a `style` element within the `head` element.

```html
    <head>
        <meta charset="UTF-8">
        <title>Cafe Menu</title>

        <style>

        </style>
    </head>
```
> **Step 12** <br>
You can add style to an element by specifying it in the `style` element and setting a property for it like this:
```html
element {
 property: value;
}
```
> Center your `h1` element by setting its `text-align` property to the value `center`.

```html
        <style>
            h1 {
                text-align: center;
            }
        </style>
```
> **Step 13** <br>
In the previous step, you used a type selector to style the `h1` element. Go ahead and center the `h2` and `p` elements with a new type selector for each one.
```html
element {
 property: value;
}
```
> Center your `h1` element by setting its `text-align` property to the value `center`.

```html
        <style>
            h1 {
                text-align: center;
            }
            h2 {
                text-align: center;
            }
            p {
                text-align: center;
            }
        </style>
```
> **Step 14** <br>
You now have three type selectors with the exact same styling. You can add the same group of styles to many elements by creating a list of selectors. Each selector is separated with commas like this:
```html
selector1, selector2 {
  property: value;
}
```
> Delete the three existing type selectors and replace them with one selector list that centers the text for the `h1`, `h2`, and `p` elements.

```html
#index.html
        <style>
            h1, h2, p {
                text-align: center;
            }
        </style>
```
> **Step 15** <br>
You have styled three elements by writing CSS inside the `style` tags. This works, but since there will be many more styles, it's best to put all the styles in a separate file and link to it.<br>
We have created a separate `styles.css` file for you and switched the editor view to that file. You can change between files with the tabs at the top of the editor.<br>
Start by rewriting the styles you have created into the `styles.css` file. Make sure to exclude the opening and closing `style` tags.

```css
#styles.css
            h1, h2, p {
                text-align: center;
            }
```
> **Step 16** <br>
Now that you have the CSS in the `styles.css` file, go ahead and remove the `style` element and all its content. Once it is removed, the text that was centered will shift back to the left.

```html
#index.html
  <head>
    <meta charset="utf-8" />
    <title>Cafe Menu</title>

  </head>
```
> **Step 17** <br>
Now you need to link the `styles.css` file so the styles will be applied again. Nest a self-closing `link` element in the `head` element. Give it a `rel` attribute value `stylesheet` and an `href` attribute value of<br>
`styles.css`.

```html
#index.html
  <head>
    <meta charset="utf-8" />
    <title>Cafe Menu</title>
    <link rel="stylesheet" href="styles.css">
  </head>
```
> **Step 18** <br>
For the styling of the page to look similar on mobile as it does on a desktop or laptop, you need to add a `meta` element with a special `content` attribute.<br>
Add the following within the `head` element:
```html
#index.html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

```html
#index.html
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta charset="utf-8" />
    <title>Cafe Menu</title>
    <link rel="stylesheet" href="styles.css">
  </head>
```
> **Step 19** <br>
The text is centered again so the link to the CSS file is working. Add another style to the file that changes the `background-color` property to `brown` for the `body` element.

```css
#styles.css
h1, h2, p {
  text-align: center;
}

body {
  background-color: brown;
}
```
> **Step 20** <br>
That brown background makes it hard to read the text. Change the `body` element's background color to be `burlywood` so it has some color but you are still be able to read the text.

```css
#styles.css
h1, h2, p {
  text-align: center;
}

body {
  background-color: burlywood;
}
```
> **Step 21** <br>
The `div` element is used mainly for design layout purposes unlike the other content elements you have used so far. Add a `div` element inside the `body` element and then move all the other elements inside the new `div`.

```html
#index.html
  <body>

    <div>
    <header>
      <h1>CAMPER CAFE</h1>
      <p>Est. 2020</p>
    </header>
    <main>
      <section>
        <h2>Coffee</h2>
      </section>
    </main>
    </div>

  </body>
```
> **Step 22** <br>
The goal now is to make the `div` not take up the entire width of the page. The CSS `width` property is perfect for this. Create a new type selector in the style sheet that gives your `div` element a width of `300px`.

```css
#styles.css
h1, h2, p {
  text-align: center;
}
div {
  width: 300px;
}
body {
  background-color: burlywood;
}
```
> **Step 23** <br>
Comments in CSS look like this:
```css
/* comment here */
```
In your style sheet, comment out the line containing the `background-color` property and value, so you can see the effect of only styling `div` element. This will make the background white again.

```css
#styles.css
body {
  /* background-color: burlywood; */
}
```
> **Step 24** <br>
Now use the existing `div` selector to set the background color of the `div` element to be `burlywood`.

```css
#styles.css
div {
    width: 300px;
    background-color: burlywood;
}
```
> **Step 25** <br>
Now it's easy to see that the text is centered inside the `div` element. Currently, the width of the `div` element is specified in pixels (`px`). Change the `width` property's value to be `80%`, to make it 80% the width of its parent element (`body`).

```css
#styles.css
div {
    width: 80%;
    background-color: burlywood;
}
```
> **Step 26** <br>
Next, you want to center the `div` horizontally. You can do this by setting its `margin-left` and `margin-right` properties to `auto`. Think of the margin as invisible space around an element. Using these two margin properties, center the `div` element within the `body` element.

```css
#styles.css
div {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
}
```
> **Step 27** <br>
So far you have been using type selectors to style elements. A *class selector* is defined by a name with a dot directly in front of it, like this:
```css
.class-name {
  styles
}
```
> Change the existing `div` selector into a class selector by replacing `div` with a class named `menu`.

```css
#styles.css
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
}
```
> **Step 28** <br>
To apply the class's styling to the `div` element, add a `class` attribute to the `div` element's opening tag and set its value to `menu`.

```html
#index.html
    <div class="menu">
```
> **Step 29** <br>
Since the cafe's main product for sale is coffee, you could use an image of coffee beans for the background of the page.<br>
Delete the comment and its contents inside the `body` type selector. Now add a `background-image` property and set its value to `url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg)`.

```css
#styles.css
body {
    background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
}
```
> **Step 30** <br>
It’s looking good. Time to start adding some menu items. Add an empty `article` element under the `Coffee` heading. It will contain a flavor and price of each coffee you currently offer.

```html
#index.html
          <h2>Coffee</h2>
          <article></article>
```
> **Step 31** <br>
`article` elements commonly contain multiple elements that have related information. In this case, it will contain a coffee flavor and a price for that flavor. Nest two `p` elements inside your `article` element. The first one's text should be `French Vanilla`, and the second's text `3.00`.

```html
#index.html
          <article>
            <p>French Vanilla</p>
            <p>3.00</p>
          </article>
```
> **Step 32** <br>
Starting below the existing coffee/price pair, add the following coffee and prices using `article` elements with two nested `p` elements inside each. As before, the first `p` element's text should contain the coffee flavor and the second `p` element's text should contain the price.<br>
`Caramel Macchiato` | `3.75` <br>
`Pumpkin Spice` | `3.50` <br>
`Hazelnut` | `4.00` <br>
`Mocha` | `4.50` <br>

```html
#index.html
    <article>
        <p>French Vanilla</p>
        <p>3.00</p>
    </article>
    <article>
        <p>Caramel Macchiato</p>
        <p>3.75</p>
    </article>
    <article>
        <p>Pumpkin Spice</p>
        <p>3.50</p>
    </article>
    <article>
        <p>Hazelnut</p>
        <p>4.00</p>
    </article>
    <article>
        <p>Mocha</p>
        <p>4.50</p>
    </article>
```
> **Step 33** <br>
The flavors and prices are currently stacked on top of each other and centered with their respective `p` elements. It would be nice if the flavor was on the left and the price was on the right.<br>
Add the class name `flavor` to the `French Vanilla` `p` element.

```html
#index.html
            <p class="flavor">French Vanilla</p>
            <p>3.00</p>
```
> **Step 34** <br>
Using your new `flavor` class as a selector, set the `text-align` property's value to `left`.

```css
#styles.css
.flavor {
  text-align: left;
}
```
> **Step 35** <br>
Next, you want to align the price to the right. Add a class named `price` to your `p` element that has `3.00` as its text.

```html
#index.html
            <p class="price">3.00</p>
```
> **Step 36** <br>
Now align the text to the `right` for the elements with the `price` class.

```css
#styles.css
.price {
  text-align: right;
}
```
> **Step 37** <br>
That is kind of what you want, but now it would be nice if the flavor and price were on the same line. `p` elements are *block-level* elements, so they take up the entire width of their parent element.<br>
To get them on the same line, you need to apply some styling to the `p` elements, so they behave more like inline elements. Add a `class` attribute with the value `item` to the first `article` element under the `Coffee` heading.

```html
#index.html
          <h2>Coffee</h2>
          <article class="item">
            <p class="flavor">French Vanilla</p>
            <p class="price">3.00</p>
          </article>
```
> **Step 38** <br>
The `p` elements are nested in an `article` element with the class attribute of `item`. You can style all the `p` elements nested anywhere in elements with a class named `item` like this:
```css
.item p { }
```
Using the above selector, add a `display` property with value `inline-block` so the `p` elements behave more like inline elements.

```css
#styles.css
.item p {
  display: inline-block;
}
```
> **Step 39** <br>
That's closer, but the price didn't stay over on the right. This is because `inline-block` elements only take up the width of their content. To spread them out, add a `width` property to the `flavor` and `price` class selectors that have a value of `50%` each.

```css
#styles.css
.flavor {
  text-align: left;
  width: 50%;
}

.price {
  text-align: right;
  width: 50%;
}
```
> **Step 40** <br>
Well that did not work. Styling the `p` elements as `inline-block` and placing them on separate lines in the code creates an extra space to the right of the first `p` element, causing the second one to shift to the next line. One way to fix this is to make each `p` element's width a little less than `50%`.<br>
Change the `width` value to `49%` for each class to see what happens.

```css
#styles.css
.flavor {
  text-align: left;
  width: 49%;
}

.price {
  text-align: right;
  width: 49%;
}
```
> **Step 41** <br>
That worked, but there is still a little space on the right of the price.<br>
You could keep trying various percentages for the widths. Instead, simply move the price `p` element to be on the same line and make sure there is no space between them.

```html
#index.html
            <p class="flavor">French Vanilla</p><p class="price">3.00</p>
```
> **Step 42** <br>
Now go ahead and change both the `flavor` and `price` class' widths to be `50%` again.

```css
#styles.css
.flavor {
  text-align: left;
  width: 50%;
}

.price {
  text-align: right;
  width: 50%;
}
```
> **Step 43** <br>
Now that you know it works, you can change the remaining `article` and `p` elements to match the first set. Start by adding the class `item` to the other `article` elements.

```html
#index.html
          <article class="item">
            <p class="flavor">Caramel Macchiato</p>
            <p class="price">3.75</p>
          </article>
          <article class="item">
            <p class="flavor">Pumpkin Spice</p>
            <p class="price">3.50</p>
          </article>
          <article class="item">
            <p class="flavor">Hazelnut</p>
            <p class="price">4.00</p>
          </article>
          <article class="item">
            <p class="flavor">Mocha</p>
            <p class="price">4.50</p>
          </article>
```
> **Step 44** <br>
Next, position the other `p` elements to be on the same line with no space between them.

```html
#index.html
          <article class="item">
            <p>Caramel Macchiato</p><p>3.75</p>
          </article>
          <article class="item">
            <p>Pumpkin Spice</p><p>3.50</p>
          </article>
          <article class="item">
            <p>Hazelnut</p><p>4.00</p>
          </article>
          <article class="item">
            <p>Mocha</p><p>4.50</p>
          </article>
```
> **Step 45** <br>
To complete the styling, add the applicable class names `flavor` and `price` to all the remaining `p` elements.

```html
#index.html
          <article class="item">
            <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
          </article>
          <article class="item">
            <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
          </article>
          <article class="item">
            <p class="flavor">Hazelnut</p><p class="price">4.00</p>
          </article>
          <article class="item">
            <p class="flavor">Mocha</p><p class="price">4.50</p>
          </article>
```
> **Step 46** <br>
If you make the width of the page preview smaller, you will notice at some point, some of the text on the left starts wrapping around to the next line. This is because the width of the `p` elements on the left side can only take up `50%` of the space.<br>
Since you know the prices on the right have significantly fewer characters, change the `flavor` class `width` value to be `75%` and the `price` class `width` value to be `25%`.

```css
#styles.css
.flavor {
  text-align: left;
  width: 75%;
}

.price {
  text-align: right;
  width: 25%;
}
```
> **Step 47** <br>
You will come back to styling the menu in a few steps, but for now, go ahead and add a second `section` element below the first for displaying the desserts offered by the cafe.

```html
#index.html
        <section>
          <h2>Coffee</h2>
          <article class="item">
            <p class="flavor">French Vanilla</p><p class="price">3.00</p>
          </article>
          <article class="item">
            <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
          </article>
          <article class="item">
            <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
          </article>
          <article class="item">
            <p class="flavor">Hazelnut</p><p class="price">4.00</p>
          </article>
          <article class="item">
            <p class="flavor">Mocha</p><p class="price">4.50</p>
          </article>
        </section>

        <section>
        </section>
```
> **Step 48** <br>
Add an `h2` element in the new section and give it the text `Desserts`.

```html
#index.html
        <section>
          <h2>Desserts</h2>
        </section>
```
> **Step 49** <br>
Add an empty `article` element under the `Desserts` heading. Give it a `class` attribute with the value `item`.

```html
#index.html
          <h2>Desserts</h2>
          <article class="item">
          </article>
```
> **Step 50** <br>
Nest two `p` elements inside your `article` element. The first one's text should be `Donut`, and the second's text `1.50`. Put both of them on the same line making sure there is no space between them.

```html
#index.html
          <article class="item">
            <p>Donut</p>
            <p>1.50</p>
          </article>
```
> **Step 51** <br>
For the two `p` elements you just added, add `dessert` as the value of the first `p` element's `class` attribute and the value `price` as the second `p` elements `class` attribute.

```html
#index.html
            <p class="dessert">Donut</p><p class="price">1.50</p>
```
> **Step 52** <br>
Something does not look right. You added the correct `class` attribute value to the `p` element with `Donut` as its text, but you have not defined a selector for it.<br>
Since the `flavor` class selector already has the properties you want, just add the `dessert` class name to it.

```css
#styles.css
.flavor, .dessert {
  text-align: left;
  width: 75%;
}
```
> **Step 53** <br>
Below the dessert you just added, add the rest of the desserts and prices using three more `article` elements, each with two nested `p` elements. Each element should have the correct dessert and price text, and all of them should have the correct classes.<br>
`Cherry Pie` | `2.75` <br>
`Cheesecake` | `3.00` <br>
`Cinnamon Roll` | `2.50` <br>

```html
#index.html
          <article class="item">
            <p class="dessert">Donut</p><p class="price">1.50</p>
          </article>
          <article class="item">
            <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
          </article>
          <article class="item">
            <p class="dessert">Cheesecake</p><p class="price">3.00</p>
          </article>
          <article class="item">
            <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
          </article>
```
> **Step 54** <br>
You can give your menu some space between the content and the sides with various `padding` properties.<br>
Give the `menu` class a `padding-left` and a `padding-right` with the same value `20px`.

```css
#styles.css
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding-left: 20px;
  padding-right: 20px;
}
```
> **Step 55** <br>
That looks better. Now try to add the same `20px` padding to the `top` and `bottom` of the menu.

```css
#styles.css
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 20px;
  padding-bottom: 20px;
}
```
> **Step 56** <br>
Since all 4 sides of the menu have the same internal spacing, go ahead and delete the four properties and use a single `padding` property with the value `20px`.

```css
#styles.css
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding: 20px;
}
```
> **Step 57** <br>
The current width of the menu will always take up 80% of the `body` element's width. On a very wide screen, the coffee and dessert appear far apart from their prices.<br>
Add a `max-width` property to the `menu` class with a value of `500px` to prevent it from growing too wide.

```css
#styles.css
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding: 20px;
  max-width: 500px;
}
```
> **Step 58** <br>
You can change the `font-family` of text, to make it look different from the default font of your browser. Each browser has some common fonts available to it.<br>
Change all the text in your `body`, by adding a `font-family` property with the value `sans-serif`. This is a fairly common font that is very readable.

```css
#styles.css
body {
  background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);

  font-family: sans-serif;
}
```
> **Step 59** <br>
It is a bit boring for all the text to have the same `font-family`. You can still have the majority of the text `sans-serif` and make just the `h1` and `h2` elements different using a different selector.<br>
Style both the `h1` and the `h2` elements so that only these elements' text use `Impact` font.

```css
#styles.css
h1, h2 {
  font-family: Impact;
}
```
> **Step 60** <br>
You can add a fallback value for the font-family by adding another font name separated by a comma. Fallbacks are used in instances where the initial is not found/available.<br>
Add the fallback font `serif` after the `Impact` font.

```css
#styles.css
h1, h2 {
  font-family: Impact, serif;
}
```
> **Step 61** <br>
Make the `Est. 2020` text italicized by creating an `established` class selector and giving it the `font-style` property with the value `italic`.

```css
#styles.css
.established {
  font-style: italic;
}
```
> **Step 62** <br>
Now apply the `established` class to the `Est. 2020` text.

```html
#index.html
      <header>
        <h1>CAMPER CAFE</h1>
        <p class="established">Est. 2020</p>
      </header>
```
> **Step 63** <br>
The typography of heading elements (e.g. `h1`, `h2`) is set by default values of users' browsers.<br>
Add two new type selectors (`h1` and `h2`). Use the `font-size` property for both, but use the value `40px` for the `h1` and `30px` for the `h2`.

```css
#styles.css
h1 {
  font-size: 40px;
}

h2 {
  font-size: 30px;
}
```
> **Step 64** <br>
Add a `footer` element below the `main` element, where you can add some additional information.

```html
#index.html
      <main>
        <section>
          <h2>Coffee</h2>
          <article class="item">
            <p class="flavor">French Vanilla</p><p class="price">3.00</p>
          </article>
          <article class="item">
            <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
          </article>
          <article class="item">
            <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
          </article>
          <article class="item">
            <p class="flavor">Hazelnut</p><p class="price">4.00</p>
          </article>
          <article class="item">
            <p class="flavor">Mocha</p><p class="price">4.50</p>
          </article>
        </section>
        <section>
          <h2>Desserts</h2>
          <article class="item">
            <p class="dessert">Donut</p><p class="price">1.50</p>
          </article>
          <article class="item">
            <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
          </article>
          <article class="item">
            <p class="dessert">Cheesecake</p><p class="price">3.00</p>
          </article>
          <article class="item">
            <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
          </article>
        </section>
      </main>

      <footer>

      </footer>
```
> **Step 65** <br>
Inside the `footer`, add a `p` element. Then, nest an anchor (`a`) element in the `p` that links to `https://www.freecodecamp.org` and has the text `Visit our website`.

```html
#index.html
      <footer>
        <p><a href="https://www.freecodecamp.org">Visit our website</a></p>
      </footer>
```
> **Step 66** <br>
Add a second `p` element below the one with the link and give it the text `123 Free Code Camp Drive`.

```html
#index.html
        <p>
          <a href="https://www.freecodecamp.org" target="_blank">Visit our website</a>
        </p>
        <p>123 Free Code Camp Drive</p>    
```
> **Step 67** <br>
You can use an `hr` element to display a divider between sections of different content.<br>
First, add an `hr` element between the first `header` element and the `main` element. Note that `hr` elements are self closing.

```html
#index.html
      <header>
        <h1>CAMPER CAFE</h1>
        <p class="established">Est. 2020</p>
      </header>

      <hr>

      <main>
        <section>
          <h2>Coffee</h2>
          <article class="item">
            <p class="flavor">French Vanilla</p><p class="price">3.00</p>
          </article>
          <article class="item">
            <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
          </article>
          <article class="item">
            <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
          </article>
          <article class="item">
            <p class="flavor">Hazelnut</p><p class="price">4.00</p>
          </article>
          <article class="item">
            <p class="flavor">Mocha</p><p class="price">4.50</p>
          </article>
        </section>
        <section>
          <h2>Desserts</h2>
          <article class="item">
            <p class="dessert">Donut</p><p class="price">1.50</p>
          </article>
          <article class="item">
            <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
          </article>
          <article class="item">
            <p class="dessert">Cheesecake</p><p class="price">3.00</p>
          </article>
          <article class="item">
            <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
          </article>
        </section>
      </main>   
```
> **Step 68** <br>
The default properties of an `hr` element will make it appear as a thin light grey line. You can change the height of the line by specifying a value for the `height` property.<br>
Change the height of the `hr` element to be `3px`.

```css
#styles.css
hr {
  height: 3px;
}
```
> **Step 69** <br>
Change the background color of the `hr` element to `brown` so it matches the color of the coffee beans.

```css
#styles.css
hr {
  height: 3px;
  background-color: brown;
}
```
> **Step 70** <br>
Notice the grey color along the edges of the line. Those edges are known as *borders*. Each side of an element can have a different color or they can all be the same.<br>
Make all the edges of the `hr` element the same color as the background of it using the `border-color` property.

```css
#styles.css
hr {
  height: 3px;
  background-color: brown;
  border-color: brown;
}
```
> **Step 71** <br>
Notice how the thickness of the line looks bigger? The default value of a property named `border-width` is `1px` for all edges of `hr` elements. By changing the border to the same color as the background, the total height of the line is `5px` (`3px` plus the top and bottom border width of `1px`).<br>
Change the `height` property of the `hr` to be `2px`, so the total height of it becomes `4px`.

```css
#styles.css
hr {
  height: 2px;
  background-color: brown;
  border-color: brown;
}
```
> **Step 72** <br>
Go ahead and add another `hr` element between the `main` element and the `footer` element.

```html
#index.html
      <main>
        <section>
          <h2>Coffee</h2>
          <article class="item">
            <p class="flavor">French Vanilla</p><p class="price">3.00</p>
          </article>
          <article class="item">
            <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
          </article>
          <article class="item">
            <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
          </article>
          <article class="item">
            <p class="flavor">Hazelnut</p><p class="price">4.00</p>
          </article>
          <article class="item">
            <p class="flavor">Mocha</p><p class="price">4.50</p>
          </article>
        </section>
        <section>
          <h2>Desserts</h2>
          <article class="item">
            <p class="dessert">Donut</p><p class="price">1.50</p>
          </article>
          <article class="item">
            <p class="dessert">Cherry Pie</p><p class="price">2.75</p>
          </article>
          <article class="item">
            <p class="dessert">Cheesecake</p><p class="price">3.00</p>
          </article>
          <article class="item">
            <p class="dessert">Cinnamon Roll</p><p class="price">2.50</p>
          </article>
        </section>
      </main>
      
      <hr>

      <footer>
        <p>
          <a href="https://www.freecodecamp.org" target="_blank">Visit our website</a>
        </p>
        <p>123 Free Code Camp Drive</p>
      </footer>
```
> **Step 73** <br>
To create a little more room around the menu, add `20px` of space on the inside of the `body` element by using the `padding` property.

```css
#styles.css
body {
  background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
  font-family: sans-serif;
  padding: 20px;
}
```
> **Step 74** <br>
Focusing on the menu items and prices, there is a fairly large gap between each line.<br>
Target all the `p` elements nested in elements with the `class` named `item` and set their top and bottom margin to be `5px`.

```css
#styles.css
h1, h2 {
  font-family: Impact, serif;
}

.item p {
  display: inline-block;
  margin-top: 5px;
  margin-bottom: 5px;
}

.flavor, .dessert {
  text-align: left;
  width: 75%;
}

.price {
  text-align: right;
  width: 25%
}
```
> **Step 75** <br>
Using the same style selector in the previous step, make the font size of the items and prices larger by using a value of `18px`.

```css
#styles.css
.item p {
  display: inline-block;
  margin-top: 5px;
  margin-bottom: 5px;
  font-size: 18px;
}
```
> **Step 76** <br>
Changing the `margin-bottom` to `5px` looks great. However, now the space between the `Cinnamon Roll` menu item and the second `hr` element does not match the space between the top `hr` element and the `Coffee` heading.<br>
Add some more space by creating a class named `bottom-line` using `25px` for the `margin-top` property.

```css
#styles.css
.bottom-line {
  margin-top: 25px;
}
```
> **Step 77** <br>
Now add the `bottom-line` class to the second `hr` element so the styling is applied.

```html
#index.html
      <hr class="bottom-line">
```
> **Step 78** <br>
Next you are going to be styling the `footer` element. To keep the CSS organized, add a comment at the end of `styles.css` with the text `FOOTER`.

```css
#styles.css
/* FOOTER */
```
> **Step 79** <br>
Moving down to the `footer` element, make all the text have a value of `14px` for the font size.

```css
#styles.css
footer {
  font-size: 14px;
}
```
> **Step 80** <br>
The default color of a link that has not yet been clicked on is typically blue. The default color of a link that has already been visited from a page is typically purple.<br>
To make the `footer` links the same color regardless if a link has been visited, use a type selector for the anchor element (`a`) and use the value `black` for the `color` property.

```css
#styles.css
a {
  color: black;
}
```
> **Step 81** <br>
You change properties of a link when the link has actually been visited by using a *pseudo-selector* that looks like `a:visited { propertyName: propertyValue; }`.<br>
Change the color of the footer `Visit our website` link to be `grey` when a user has visited the link.

```css
#styles.css
a:visited {
  color: grey;
}
```
> **Step 82** <br>
You change properties of a link when the mouse hovers over them by using a *pseudo-selector* that looks like `a:hover { propertyName: propertyValue; }`.<br>
Change the color of the footer `Visit our website` link to be `brown` when a user hovers over it.

```css
#styles.css
a:hover {
  color: brown;
}
```
> **Step 83** <br>
You change properties of a link when the link is actually being clicked by using a *pseudo-selector* that looks like `a:active { propertyName: propertyValue; }`.
<br>
Change the color of the footer `Visit our website` link to be `white` when clicked on.

```css
#styles.css
a:active {
  color: white;
}
```
> **Step 84** <br>
To keep with the same color theme you have already been using (black and brown), change the color for when the link is visited to `black` and use `brown` for when the link is actually clicked.

```css
#styles.css
a:visited {
  color: black;
}

a:hover {
  color: brown;
}

a:active {
  color: brown;
}
```
> **Step 85** <br>
The menu text `CAMPER CAFE` has a different space from the top than the address's space at the bottom of the menu. This is due to the browser having some default top margin for the `h1` element.<br>
Change the top margin of the `h1` element to `0` to remove all the top margin.

```css
#styles.css
h1 {
  font-size: 40px;
  margin-top: 0;
}
```
> **Step 86** <br>
To remove some of the vertical space between the `h1` element and the text `Est. 2020`, change the bottom margin of the `h1` to `15px`.

```css
#styles.css
h1 {
  font-size: 40px;
  margin-top: 0;
  margin-bottom: 15px;
}
```
> **Step 87** <br>
Now the top spacing looks good. The space below the address at the bottom of the menu is a little bigger than the space at the top of the menu and the `h1` element.<br>
To decrease the default margin space below the address `p` element, create a class selector named `address` and use the value `5px` for the `margin-bottom` property.

```css
#styles.css
.address {
  margin-bottom: 5px;
}
```
> **Step 88** <br>
Now apply the `address` class to the `p` element containing the address.

```html
#index.html
      <footer>
        <p>
          <a href="https://www.freecodecamp.org" target="_blank">Visit our website</a>
        </p>
        <p class="address">123 Free Code Camp Drive</p>
      </footer>
```
> **Step 89** <br>
The menu looks good, but other than the coffee beans background image, it is mainly just text.<br>
Under the `Coffee` heading, add an image using the url `https://cdn.freecodecamp.org/curriculum/css-cafe/coffee`.jpg. Give the image an `alt` value of `coffee icon`.

```html
#index.html
          <h2>Coffee</h2>
          <img src="https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg" alt="coffee icon">
```
> **Step 90** <br>
The image you added is not centered horizontally like the `Coffee` heading above it. `img` elements are "like" inline elements.<br>
To make the image behave like heading elements (which are block-level), create an `img` type selector and use the value `block` for the display property and use the applicable `margin-left` and `margin-right` values to center it horizontally.

```css
#styles.css
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
```
> **Step 91** <br>
Add one last image under the `Desserts` heading using the url `https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg`. Give the image an `alt` value of `pie icon`.

```html
#index.html
          <h2>Desserts</h2>
          <img src="https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg" alt="pie icon">
```
> **Step 92** <br>
It would be nice if the vertical space between the `h2` elements and their associated icons was smaller. The `h2` elements have default top and bottom margin space, so you could change the bottom margin of the `h2` elements to say `0` or another number.<br>
There is an easier way, simply add a negative top margin to the `img` elements to pull them up from their current positions. Negative values are created using a `-` in front of the value. To complete this project, go ahead and use a negative top margin of `25px` in the `img` type selector.

```css
#styles.css
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: -25px;
}
```