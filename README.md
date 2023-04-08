# FCC-FEDL-Bootstrap/jQuery

Intro to Bootstrap

- Bootsrap is a front end framework used to design responsive web pages and applications.
- It takes a 'mobile-first' approach to web development, and it includes pre-built CSS styles and classes, as well as some JS functionality.

- Add `Bootstrap` to any app by adding the following code at the top of the HTML file.

```HTML
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous"/>
```

- tags that do not require a closing tag may be closed with `>` or `/>`

## Use Responsive Design with Bootstrap Fluid Containers

- Bootstrap is a predefined CSS framework package.
- It is a popular open-source front-end development framework that provides a set of CSS, JavaScript, and HTML templates for building responsive, mobile-first web applications and websites.
- Bootstrap includes pre-built components and styles for common user interface elements such as buttons, forms, typography, navigation, and more, which developers can use to easily create modern and visually appealing designs.
- Additionally, Bootstrap also provides a responsive grid system and a collection of utility classes to help developers quickly create layouts that work well on different screen sizes and devices.
- Bootstrap will figure out how wide the screen is and respond by resizing the HTML elements.

- Get the HTML code to respond to Bootstrap by adding the appropriate `link` (shown above), and nest all HTML (all elements that you wish to respond to bootstrap fluid container) in a `div` element with `class = "container-fluid"`

## Make Images Mobile Responsive

- Use `img-responsive` in an `<img>` tag to get the image fit the exact with of the screen

```html
<img class="img-responsive" scr="https://...jpg/>
```

## Center Text with Bootstrap

- Add `class="text-center"` to an element to center the text
- Remember, several classes can be added to the same element by separating with a whitespace.

Example

```html
<h2 class="red-text text-center">Text</h2>
```

## Create a Bootstrap Button

- Bootstrap has its own `button` styles.
- Add `class="btn btn-default` to the `<button>` element
- The default buttons are only as wide as the text.

- Add another class `btn-block` to get the button to fill the width of the screen.

- change the color of the button to the primary color assigned to the CSS by replacing the `btn-default` class with `btn-primary`

```html
<button class="btn btn-primary btn-block">Like</button>
```

- Add additional buttons with pre-defined colors

- Use `btn-info` class to catch the attention of the user for optional actions.
- Note that new buttons still need `btn` and `btn-block` to match the appearance of the previous button.

```html
<button class="btn btn-block btn-info">Info</button>
```

- Use `btn-danger` class to notify users that the button performs an irrevocable action, such as 'delete'.

```html
<button class="btn btn-block btn-danger">Delete</button>
```

## Use the Bootstrap Grid Element to Put Elements Side By Side

- Bootstrap uses a responsive 12-column grid system, making it easy to put elements into rows and specify each element width.
- Most bootstrap classes can be applied to a `div` element.

- Bootstrap has different column width attributes applied based on the width of the user screen.
- One example would be `class="col-md-*"`
  - `md` refers to medium, which would correspond to laptops.
  - `xs` refers to extra small screens, such as mobile phones.
  - `*` refers to how many columns wide the element should be.

Example

```html
<div class="row">
  <div class="col-xs-4">
    <button class="btn btn-block btn-primary">Like</button>
  </div>
  <div class="col-xs-4">
    <button class="btn btn-block btn-info">Info</button>
  </div>
  <div class="col-xs-4">
    <button class="btn btn-block btn-danger">Delete</button>
  </div>
</div>
```

- The above code will place each button of equal width in a row

## Ditch Custom CSS for Bootstrap

- Use bootstrap's built-in styles to clean up your code

### Use a span to Target Inline Elements

- Use spans to create inline elements
  - It allows you to put several elements on the same line, and even apply different styles to different parts in the same line.

Example

```html
<p>Things cats <span class="text-danger">love</span>:</p>
```

- The above code will apply the "text-danger" font color to the text "love"

### Create a custom heading

- Bootstrap uses a responsive grid system, which makes it easy to put elements into rows and specify its relative width.
- Most bootstrap classes can be applied to a `div` element

example

```html
<div class="container-fluid">
  <div class="row">
    <div class="col-xs-8">
      <h2 class="text-primary text-center">CatPhotoApp</h2>
    </div>
    <div class="col-xs-4">
      <a href="#"><img class="img-responsive thick-green-border" src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg" alt="A cute orange cat lying on its back."></a>
    </div>
  </div>
...
</div>
```

## Add Font Awesome Icons to Buttons

- Font Awesome is a convenient library of icons.
- These icons can be webfonts or vector graphics, and are treated just like fonts.
- Specify size using pixels, and they will assume the font size of their parent HTML elements

- Use the following code at the top of the HTML to include Font Awesome in any app

```html
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.1/css/all.css" integrity="sha384-50oBUHEmvpQ+1lW4y57PTFmhCaXp0ML5d60M1M7uH2+nqUivzIebhndOJK28anvf" crossorigin="anonymous">
```

- `i` was commonly used to make text elements italic, but it is now generally used for `icons`

example

```html
<i class="fas fa-thumbs-up"></i>
<i class="fas fa-info-circle"></i>
<i class="fas fa-trash"></i>
```

- Note that the icon font can be placed before or after the text, and the text does not have to wrapped in the `<i>` tags.

```html
<button class="btn btn-block btn-primary"><i class="fas fa-thumbs-up"></i> Like</button>
```

- Remember to put a space between the text and the font icon to add space.

## Responsively Style Radio Buttons/Checkboxes

- Use `col-xs-*` class on `form` elements to evenly spread out radio buttons across the page, regardless of the screen size

```html
<div class="row">   
  <div class="col-xs-6">
    <label><input type="radio" name="indoor-outdoor"> Indoor</label>
  </div>
  <div class="col-xs-6">
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label>
  </div>
</div>
```

- nest all elements you wish to apply bootstrap to with `<div class="row">`
- nest each element within `<div class="row">` with `<div class="col-xx-*">`

## Style Text Inputs as Form Controls

- Use `form-control` class on textual `inputs`, `textarea`, and `select` elements to achieve consistent styling throughout the page.
- When applied, the applicable element will have 100% width

```html
<input type="text" class="form-control" placeholder="cat photo URL" required>
```

## Line up Form Elements Responsively with Bootstrap

- Use `<div class="row">` and `<div class="col-xx-*>"` to place form elements such as inputs and buttons in-line.

```html
<div class="row">
  <div class="col-xs-7">
    <input type="text" class="form-control" placeholder="cat photo URL" required>
  </div>
  <div class="col-xs-5">
    <button type="submit" class="btn btn-primary"><i class="fa fa-paper-plane"></i> Submit</button>
  </div>
</div>
```

---

- From here on, the use of jQuery and Bootstrap in HTML and CSS will be introduced

- The following is a general format for applying Bootstrap to HTML

```html
<div class="container-fluid">
  <h3 class="text-primary text-center">jQuery Playground</h3>
  <div class="row">
    <div class="col-xs-6">
      <h4>#left-well</h4>
      <div class="well" id="left-well">
        <button class="btn btn-default target" id="target1">#target1</button>
        <button class="btn btn-default target" id="target2">#target2</button>
        <button class="btn btn-default target" id="target3">#target3</button>
      </div>
    </div>
    <div class="col-xs-6">
      <h4>#right-well</h4>
      <div class="well" id="right-well">
        <button class="btn btn-default target" id="target4">#target4</button>
        <button class="btn btn-default target" id="target5">#target5</button>
        <button class="btn btn-default target" id="target6">#target6</button>
      </div>
    </div>
  </div>
</div>
```

## Learn How Script Tas and Document Ready Work

- In order to use jQuery, we need to add some things to the HTML code
- We need a `<script>` element. The browser will run any JS code inside a `<script>` element, including jQuery.
- Inside the `<script>` element, add the following

```html
<script>
  $(document).ready(function() {

  });
</script>
```

- It is important to note that the code inside the `function` will run as soon as the browser loads the page.
- This is important because without the `document ready function`, the code may run before the HTML is rendered, which could lead to bugs.

## Target HTML Elements with Selectors Using jQuery

- All jQuery functions start with a `$`, referred to as the dollar sign operator, or just `bling`
- jQuery often selects an HTML element with a selector and does something with it.
- For example, in order to make the `button` elements bounce, add the following code to the `document ready function`.

```js
$("button").addClass("animated bounce");
```

- Note that jQuery library and Animate.css library must be included in the code to access its features.

## Target Elements by Class/id Using jQuery

- Use `$(" ")` to select an element, a class, or id.
- Just like in css, use `.` to access a class, and `#` to access an id.
- then add `.addClass(" ")` to add the desired css feature.

```html
<script>
  $(document).ready(function() {
    $("button").addClass("animated bounce");
    $(".well").addClass("animated shake");
    $("#target3").addClass("animated fadeout")
  });
</script>
```

## Target te Same Element with Multiple jQuery Selectors

- The above example shows the different methods of targeting elements - type, class, and id
- It is possible to add multiple classes in a single `addClass()`, but there is another way to apply multiple classes to elements

```html
<script>
  $(document).ready(function() {
    $("button").addClass("animated"); // targets all button elements
    $(".btn").addClass("shake");      // targets class .btn
    $("#target1").addClass("btn-primary") // targets id target1
  });
</script>
```

## Remove Classes from an Element with jQuery

- In order to remove classes from an element, use the same method used to add classes to an element.

```html
<script>
  $(document).ready(function() {
    $("button").addClass("animated bounce");
    $(".well").addClass("animated shake");
    $("#target3").addClass("animated fadeOut");
    $("button").removeClass("btn-default");   // use 'removeClass()'
  });
</script>
```

## Change the CSS of an Element using jQuery

- Change the css of an HTML element directly with jQuery by using `.css()` function.

```html
<script>
  $(document).ready(function() {
    $("#target1").css("color", "red");
  });
</script>
```

- the format is slightly different from a regular CSS declaration
  - the property and its values are in quotes
  - separated with comma rather than a colon

## Disable an Element using jQuery

- change non-CSS properties of HTML elements with jQuery, such as disabling buttons.
- use the `.prop()` function to adjust the properties of elements

```html
<script>
  $(document).ready(function() {
    $("#target1").prop("disabled", true);
  });
</script>
```

## Change Text Inside an Element using jQuery

- Change the text between the start and end tags of an element using jQuery. You can also change HTML markup.
- Use `.html()` function to add HTML tags and text within an element.
- Any previous element content will be replaced with the new input content.

- jQuery also has a similar function called `.text()`, which only alters the text without adding tags.
- i.e., it will not apply any HTML tags passed to it.

```html
<script>
  $(document).ready(function() {
    $("#target1").css("color", "red");      
    $("#target4").html("<em>#target4</em>") // This will emphasize the text '#target4'.
                                            // if you replace the `.html()` with `.text()`, it will display '<em>#target4</em>`
  });
</script>
```

## Use appendTo to Move Elements with jQuery

- use `.appendTo()` function to move elements from one div to another.

```html
<script>
  $(document).ready(function() {
    $("#target2").appendTo("#right-well")
  });
</script>
```

- `#target2` was initially in the div containing `<h4>#left-well<h4>`
- `.appendTo("#right-well")` will move `#target2` to the div containing `<h4>#right-well</h4>`