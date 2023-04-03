# FCC-FEDL-Bootstrap

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