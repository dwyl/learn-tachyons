# Learn Tachyons
[Help Wanted!] Learn how to use Tachyons to craft beautiful, responsive &amp; fast UI with minimal CSS!

## What?

![tachyons](https://cloud.githubusercontent.com/assets/14013616/20138900/0c07e07a-a67b-11e6-80a2-a0ff6b335712.jpg)

Tachyons is a css framework to craft beautiful, responsive & fast UIs with minimal CSS!

Tachyons embraces a different style than many popular css frameworks known as `Functional CSS`. But how is it different?

Here's a some CSS for a bootstrap `primary` button:

![btn](https://cloud.githubusercontent.com/assets/14013616/20070844/eec73158-a519-11e6-9011-5b8cc14f73ac.png)

```css
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}

.btn {
  display: inline-block;
  padding: 6px 12px;
  margin-bottom: 0;
  font-size: 14px;
  font-weight: 400;
  line-height: 1.42857143;
  text-align: center;
  white-space: nowrap;
  vertical-align: middle;
  -ms-touch-action: manipulation;
  touch-action: manipulation;
  cursor: pointer;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 4px;
}
```

What a monolith! There's a lot of CSS attributes there; Bootstrap is quite opinionated about how a button should look and function.

What if we wanted a button that looks a little different? We'd most likely need to add another class:

```css
.btn-dwyl {
  background-color: #46B6AC;
  border-color: #46B6AC;
  padding: 10px;
  text-transform: uppercase;
  letter-spacing: 4px;
  font-weight: 300;
}
```

![btn-dwyl](https://cloud.githubusercontent.com/assets/14013616/20138059/1501dfb4-a676-11e6-8c74-750b5be89d88.png)

Tachyons approaches this with `single utility classes` (classes that do one thing). Change the `html`, not the `stylesheet`:

```html
<button class="pa2 br2 bg-green tc tracked">do what you love</button>
```

Each class has one responsibility:

+ `pa2` - "padding all 2"
+ `br2` - "border radius 2"
+ `bg-green` - "background color green"
+ `tc` - "text align center"
+ `tracked` - "with letter spacing"

## Why Functional CSS?

![fcss](https://cloud.githubusercontent.com/assets/14013616/20139391/cdeed714-a67d-11e6-9363-9b90749d3054.png)

You may be thinking:
+ Just how does this make my CSS better?
+ Why use this approach when CSS has been written like the bootstrap example for years?
+ Isn't this just like using inline styles? ([considered by many to be bad practice in CSS](http://stackoverflow.com/questions/2612483/whats-so-bad-about-in-line-css))
+ Won't I end up repeating myself in the html?

Let's have a look at some of the core features and ideas of `Functional CSS` and see if we can answer some of those questions:

## Functional CSS is:

### Functional :innocent:

Small, clear, easy to read classes that are easy to apply and do one thing. Having small classes means it's easy to make a set of consistent spacing and type rules - you end up forcing a beautiful type scale & rhythm on your design.

> "Good design (my preferred school of good design, at least) is mathsy, rational and pure —and CSS is design— so it follows that there are a bunch of lessons we can bring back from FP land into design." - [Jon Gold](http://www.jon.gold/2015/07/functional-css/)

### Composable :musical_score: :notes: :musical_keyboard:

In Functional Programming you combine (or compose) a bunch of tiny functions together to do bigger things (like lots of notes to make music!). You end up reusing a lot of your code which is great for performance and consistency! Just like the button example:

```html
<button class="pa2 br2 bg-green tc tracked"> <!--VS--> <button class="btn btn-dwyl">
```

We'll end up reusing :recycle: nearly all of those classes, whereas the button classes will only be used for buttons.

Be green! Recycle your classes!

![recycle-your-classes](https://cloud.githubusercontent.com/assets/14013616/20142303/10aeccc2-a68c-11e6-98dc-f082242d617d.jpg)

> "Doing one thing extremely well promotes reusability and reduces repetition." - [Adam Morse](https://github.com/tachyons-css/tachyons/)

### Immutable :gem: :gem: :gem:

In Functional languages declaring a property means it will never get overwritten, something known as `Immutability` - i.e It can't ever be changed (or `mutated`). A huge benefit you gain from  immutability is that code is easier to reason about (you don't have to go on a hunt to find where something might have been changed).

CSS on the other hand is inherently mutable (it's the "C" in CSS - the `Cascade`)! But because `fcss` classes are `single responsibility`, they aren't at risk of overriding each other. This almost eliminates the problems of the cascade (Changing a property somewhere won't break your code elsewhere).

Another extremely useful property you gain from immutability is something called **Referential Transparency** : In other words: A thing does exactly what it says on the tin!

We know with a fair amount of confidence what our button will look like just from reading the classes:

```html
<button class="pa2 br2 bg-green tc tracked">
```

but for all we know our `.btn` & `.btn-dwyl` classes could look like:

![questionable](https://cloud.githubusercontent.com/assets/14013616/20143859/88f29ac8-a692-11e6-9980-012d3c5d1738.png)

Yikes! :open_mouth:

And what if we wanted to change it? Do we change our "monolithic" button classes and pray :pray: that they don't break other buttons elsewhere? :boom: On a BIG project?!

![lol](https://media1.giphy.com/media/sjfefACqq2BUc/200_s.gif)

Be realistic, we're likely to add more and more classes to avoid this from happening. This gets more and more wasteful over time, adding bloat to our CSS files:

> In [the monolith] model, you will never stop writing css. Refactoring css is hard and time consuming. Deleting unused css is hard and time consuming. And more often than not - it’s not work people are excited to do. So what happens? People keep writing more and more css - [Adam Morse](http://mrmrs.io/writing/2016/03/24/scalable-css/).


## Why Tachyons?

What else does Tachyons specifically give us?

### Easy to Understand and Use

A great thing about tachyons is how quickly and easily you can get up and running. The classes are easy to understand (once you get used to them), If you know CSS, you know tachyons!

If you find the names too terse you can use the [verbose version](https://github.com/tachyons-css/tachyons-display-verbose).

### Mobile First Responsive Design

By far one of the most useful features is that almost all classes have "responsive suffix" versions:

for example the "padding all 4" class `pa4` also has 3 other versions:

```css
.pa4-ns { ... }
.pa4-m { ... }
.pa4-l { ... }
```

`ns`, `m`, and `l` are short for "not small", "medium" and "large"

Tachyons gives you incredible flexibility to change your design at different screen sizes. And by default the "non suffixed" class **is** the mobile class! This encourages you to design for mobile first and expand outwards. All of this without writing a line of css! Tachyons has the referential transparency of inline styles coupled with the power of media queries!

### A Natural Workflow

Using Tachyon's styles in this way also seems to encourages a more natural workflow when building UIs

> Styles are localized at the HTML template level, rather than being controlled by central CSS files. This fits my workflow because I usually work through a website's design one page at time... - [Jason Li](http://notebook.hongkonggong.com/2016/04/21/is-tachyons-the-right-css-framework-for-me/)

Jason Li illustrates this perfectly:

![tachyonsexplanationnow](https://cloud.githubusercontent.com/assets/14013616/20149576/d5bae650-a6a9-11e6-87b2-dcb65f1dc882.png)

![tachyonsexplanationbefore](https://cloud.githubusercontent.com/assets/14013616/20149566/caf62b80-a6a9-11e6-95a9-f06af3e8413f.png)

### Works well with component based UIs

Using a templating engine or framework (such as `Rails`, `React`, `Elm`, `Angular`) means you can reduce the repetition of classes in your html by reusing them as components.

### Great Performance that Scales

As your project grows larger, your stylesheet doesn't (or only grows very minimally). This has benefits for the user as there's less CSS to download and the browser has to register less styles overall (it can cache the result of already computed styles).

> "Inline styles are 1 to 1 for the browser. i.e an inline style can only style one element at a time. While a class has a 1 to many relationship. This has non-trivial deltas in rendering speed and can greatly reduce jank in a complicated ui." - [Adam Morse](https://github.com/tachyons-css/tachyons/issues/12)

## How?

You can get up and running by just adding a link tag in your html

```html
<link rel="stylesheet" href="https://unpkg.com/tachyons@4.5.4/css/tachyons.min.css">
```

Or grab the latest version

```html
<link rel="stylesheet" href="https://unpkg.com/tachyons/css/tachyons.min.css">
```

If you want to customise the styles you can clone the tachyons repo locally and install the dependencies

```sh
$ git clone https://github.com/tachyons-css/tachyons.git
$ cd tachyons
$ npm install
```

Make the changes that you'd like to the css files and then run

```sh
$ npm run build
```

This will output both an unminified and minified css file to the `/css` directory

Check out [this video](https://vimeo.com/174698456) for a guide to setting up.

### Resources

+ [Tachyons.io](http://tachyons.io/)
+ [Tachyons Table of Styles](http://tachyons.io/docs/table-of-styles/) : http://tachyons.io/docs/table-of-styles/
+ [Tachyons Github Repo](https://github.com/tachyons-css/tachyons/) : https://github.com/tachyons-css/tachyons/
+ [Tachyons Verbose Version](https://github.com/tachyons-css/tachyons-display-verbose) : https://github.com/tachyons-css/tachyons-display-verbose
+ [Setting up Custom Tachyons Build](https://vimeo.com/174698456)

#### Articles

+ [CSS and Scalability](http://mrmrs.io/writing/2016/03/24/scalable-css/)
+ [Functional Programming, CSS, and your Sanity](http://www.jon.gold/2015/07/functional-css/) : http://www.jon.gold/2015/07/functional-css/
+ [Rationalizing Functional CSS](https://marcelosomers.com/writing/rationalizing-functional-css/) : https://marcelosomers.com/writing/rationalizing-functional-css/
+ [Building and Shipping Functional CSS](https://blog.colepeters.com/building-and-shipping-functional-css/) : https://blog.colepeters.com/building-and-shipping-functional-css/
+ [Is Tachyons the right CSS framework for me?](http://notebook.hongkonggong.com/2016/04/21/is-tachyons-the-right-css-framework-for-me/) : http://notebook.hongkonggong.com/2016/04/21/is-tachyons-the-right-css-framework-for-me/
+ [FCSS](http://eng.wealthfront.com/2013/08/20/functional-css-fcss/) : http://eng.wealthfront.com/2013/08/20/functional-css-fcss/

#### Questions and Discussions

+ [How is Tachyons different from inline styles?](https://github.com/tachyons-css/tachyons/issues/12) : https://github.com/tachyons-css/tachyons/issues/12
+ [What's so bad about inline css?](http://stackoverflow.com/questions/2612483/whats-so-bad-about-in-line-css) : http://stackoverflow.com/questions/2612483/whats-so-bad-about-in-line-css
