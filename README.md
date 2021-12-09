# Learn Tachyons [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat-square)](https://github.com/dwyl/learn-tachyons/issues) [![HitCount](http://hits.dwyl.com/dwyl/learn-tachyons.svg?style=flat-square)](http://hits.dwyl.com/dwyl/learn-tachyons)

![tachyons-intro-image](https://cloud.githubusercontent.com/assets/194400/25710569/87726714-30e4-11e7-9532-4a447bd61629.png)

_**Learn** how to use **Tachyons**
to **craft beautiful, 100% responsive,
functional** and **fast User Interface/Experience** (UI/UX)
with **minimal CSS**
in **much less time**._

<!-- START doctoc -->
- [_Why_?](#why)
  - [_One Minute Summary_](#one-minute-summary)
- [What?](#what)
  - [What is _Different_?](#what-is-different)
  - [_Bootstrap_ Custom Button (_The Old Way_!)](#bootstrap-custom-button-the-old-way)
  - [_Tachyons_ Custom Button (_New Way_!)](#tachyons-custom-button-new-way)
  - [What is "_Functional_" CSS?](#what-is-functional-css)
- [Functional CSS is:](#functional-css-is)
  - [Functional :innocent:](#functional-innocent)
  - [Composable :musical_score: :notes: :musical_keyboard:](#composable-musical_score-notes-musical_keyboard)
  - [Immutable :gem: :gem: :gem:](#immutable-gem-gem-gem)
- [Why Tachyons?](#why-tachyons)
  - [Easy to Understand and Use](#easy-to-understand-and-use)
  - [_Mobile First_ Responsive Design](#mobile-first-responsive-design)
  - [Accessibility](#accessibility)
  - [A Natural Workflow](#a-natural-workflow)
  - [Works well with component based UIs](#works-well-with-component-based-uis)
  - [Great Performance that Scales](#great-performance-that-scales)
- [_How_?](#how)
  - [Try _Before_ You Commit (3 Easy Steps)](#try-before-you-commit-3-easy-steps)
  - [In your Own Project](#in-your-own-project)
- [Learning the ropes](#learning-the-ropes)
  - [Responsive modifiers](#responsive-modifiers)
  - [Typography](#typography)
  - [Layout](#layout)
  - [Theming](#theming)
+ [Image Placeholder Example](#how-to-create-an-image-placeholder)
+ [Responsive Navigation Menu Example](#responsive-navigation-menu)
- [Resources](#resources)
  - [Articles](#articles)
  - [Questions and Discussions](#questions-and-discussions)
  - [Future of Tachyons](#future-of-tachyons)
<!-- END doctoc  -->

## _Why_?

The User Interface (UI) or User Experience (UX)
is the part of your application that
the ***people*** ("_end users_")
_**see** and **interact** with_.
Ensuring that the **UI/UX** is the _**best** it **can be**_,
is _easily_ the ***top priority*** for our Web/Mobile projects.

Without ~~good~~ ***great UI/UX***
["_**nothing `else` matters**_"](https://youtu.be/tAGnKpE4NCI)
to the person _using_ your app. <br />
The **UI/UX** is what _**matters**_,
**not** the **programming language**,
what type of **server**,
which "***front-end framework***"
or "**backend infrastructure**" you are using;
***Nobody cares*** about the "_boring technical details_",
they _only_ care about their **own _experience_** using the app/website.

![image](https://cloud.githubusercontent.com/assets/194400/25721528/adec307c-3108-11e7-8f66-10edae56e6f0.png)

### _One Minute Summary_

Through _experience_
(_building **many web/mobile** apps large and small
  in teams ranging from 2 - **200 people**_),
we have found that:
+ _**Hand-writing CSS**_ is _very **time-consuming** and **repetitive**_!
+ Using (_most_) CSS "_frameworks_" results in:
  + Lots of **Duplication** _where people re-create styles over-and-over_
  + "**_Zombie_ Code**" _unused styles that nobody will risk removing_
  + **Bloated** apps/sites that take _much_ longer
  to develop, load and maintain than they _need_ to.
+ **_Functional_ CSS** _ensures_:
  + UI is **100% _Predictable_, Consistent**
  and _free from_ (_unwanted_) "***Side Effects***"
  (_where a change in one place "breaks" something else!_)
  + It's ***immediately clear*** from reading ***one***
  block of code what the component _does_ and what it looks like.
  + **_Updates_** to UI are made in ***One Place/File***. (_see diagram below_)
  + **Time** to _develop_ your App's UI ***scales proportionally***
  instead of increasing ***exponentially*** the way it does with
  most "traditional" CSS frameworks.
  + The moment you want anything "_custom_" most CSS frameworks
  let you down _badly_ because you have to "_override_",
  Tachyons is _made_ for helping you to use your imagination!
  The resulting UI will be ***much less code***,
  load ***considerably faster*** and be ***far easier to maintain***!

Tachyons lets you avoid the "_CSS Fire_":

[![image](https://cloud.githubusercontent.com/assets/194400/25718602/9a99b3be-30fe-11e7-9462-758cef9cbe1d.png)](https://twitter.com/iamdevloper/status/753716544949981184 "CSS is easy? - click to see original tweet")

> Extended discussion on the pros/cons of
Functional CSS & Tachyons: <br />
https://github.com/dwyl/learn-tachyons/issues/1

## What?

![what-section-header](https://cloud.githubusercontent.com/assets/194400/25721712/64ec964a-3109-11e7-8395-05d928091c5c.png)

Tachyons is a **CSS _Design System_** anyone can learn/use
to craft beautiful, responsive & fast UIs with minimal CSS!
Tachyons has ***all*** the ***building blocks***
you (_your team_) need(s) to
[_build **anything** you can **imagine**_](https://youtu.be/Um-PlX6oPBQ?t=12s "The LEGO Movie Scene: I am a Master Builder!").

Tachyons embraces a different style than many popular CSS
frameworks known as "***Functional CSS***".

### What is _Different_?

When you use the Bootstrap `primary` button class in your web app,
it _looks_ simple enough on the surface,
you simply add the class to your HTML markup.
Following the example on:
https://getbootstrap.com/docs/4.0/components/buttons/

```hmtl
<button type="button" class="btn btn-primary">Primary</button>
```

![btn](https://cloud.githubusercontent.com/assets/14013616/20070844/eec73158-a519-11e6-9011-5b8cc14f73ac.png)

Here's is the CSS for that bootstrap `primary` button:

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
  line-height: 1.42857143; /* who needs this level of decimal precision in CSS?! */
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
Visit: http://getbootstrap.com/css/#buttons
(_open your "dev tools"_) then inspect one of the buttons
and see for yourself:
![image](https://cloud.githubusercontent.com/assets/194400/25717024/190df58a-30f9-11e7-8d14-522a3d3853a1.png "Twitter Bootstrap buttons - click to enlarge")


What a _monolith_! There are a _lot_ of CSS attributes there; <br />
Bootstrap is quite ***opinionated*** about how a button should
look and function.

If you want to change/customise any aspect
of the button
(_e.g: [font](https://www.cssfontstack.com/Helvetica) or
[color](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)_),
you will need to:
1. Create a new class in your `app.css` file
(_or whatever your project calls it_)
2. Define the CSS styles for that custom attribute, e.g:
```css
.custom-btn-purple-helvetica {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  color: #800080; /* wikipedia.org/wiki/The_Color_Purple */
}
```
3. Add the CSS class to the instance of the button you created.
```html
<button type="button" class="btn btn-primary custom-btn-purple-helvetica">
  Primary</button>
```
This 3-step process is slow and _always_ ends up with more
CSS than if you used pre-existing Tachyons classes. (_see below_) 🌈

### _Bootstrap_ Custom Button (_The Old Way_!)

What if we wanted a button that looks a little different?
We'd most likely need to add another class. e.g:

```html
<button type="button" class="btn btn-dwyl">do what you love</button>
```
Which requires us to write quite a lot of custom CSS:

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

### _Tachyons_ Custom Button (_New Way_!)

Tachyons approaches this with `single utility classes`
(classes that do one thing). <br />
These `single utility classes` encourage
a different way of building UI: <br />
all code is in a single place
the `html`, not the `stylesheet`:

```html
<button class="bw0 br2 bg-dwyl-teal pa2 white fw1 tc ttu tracked">do what you love</button>
```

Each class has one responsibility:
+ `bw0` - "border width 0" see:
+ `br2` - "border radius 2" see:
+ `bg-dwyl-teal` - "background color dwyl teal" (_this is an example of a custom color_)
+ `pa2` - "padding all 2"
+ `white` - "text color white"
+ `fw1` - "font weight 1"
+ `tc` - "text align center"
+ `ttu` - "text transform uppercase"
+ `tracked` - "with letter spacing"

see: `/examples/buttons.html`

**Note**: Tachyons does not have _all_-the-colors,
hence we had to define our own.
However given that there is a clear format for defining colors
we defined our own as `bg-dwyl-teal`:
```css
.bg-dwyl-teal {
  background-color: #4DB6AC;
}
```
This is "_OK_" because it's still a _single-purpose_ class
that we can _re-use_ for any elements that require the teal background.

### What is "_Functional_" CSS?

![fcss](https://cloud.githubusercontent.com/assets/194400/25721674/33bc13ac-3109-11e7-89a6-b8f09f0f4417.png)


You may be thinking:
+ How _exactly_ does this make my CSS better?
+ Why use this approach when CSS has been written
like the bootstrap example for years?
+ Isn't this just like using inline styles?
([considered by many to be bad practice in CSS](http://stackoverflow.com/questions/2612483/whats-so-bad-about-in-line-css))
+ Won't I end up _repeating myself_ in the HTML?

Let's have a look at some of the core features
and ideas of `Functional CSS` and see if we can
answer some of those questions.

## Functional CSS is:

### Functional :innocent:

Small, clear, easy to read classes that
are easy to apply and do _one_ thing. <br />
Having small classes means it's easy to make
a set of **consistent spacing and type
rules** - you end up forcing a beautiful type
scale & rhythm on your design.

> "_**Good design** (my preferred school of
good design, at least) is **mathsy**,
**rational** and **pure** —and CSS is design— so it
follows that there are a bunch of lessons
we can bring back from FP land into design_." -
[Jon Gold](http://www.jon.gold/2015/07/functional-css) Front-End Wizard @ AirBnB

### Composable :musical_score: :notes: :musical_keyboard:

In Functional Programming you combine (or compose) a bunch of tiny functions together to do bigger things (like lots of notes to make music!). You end up reusing a lot of your code which is great for **performance and consistency**! Just like the button example:

```html
<button class="pa2 br2 bg-green tc tracked"> <!--VS--> <button class="btn btn-dwyl">
```

We'll end up reusing :recycle: nearly all of those classes, whereas the button classes will only be used for buttons.

Be green! Recycle your classes!

![recycle-your-classes](https://cloud.githubusercontent.com/assets/14013616/20142303/10aeccc2-a68c-11e6-98dc-f082242d617d.jpg)

> "Doing one thing extremely well promotes reusability and reduces repetition." - [Adam Morse](https://github.com/tachyons-css/tachyons/)

### Immutable :gem: :gem: :gem:

In Functional languages declaring a property
means it will never get overwritten,
something known as `Immutability` -
i.e it can't ever be changed (_or `mutated`_).
A huge benefit you gain from  immutability is
that code is easier to reason about
(_you **don't have to** go on a **hunt** to find where
something might have been changed_).

CSS on the other hand is _inherently **mutable**_
(it's the "C" in CSS - the `Cascade`)!
But because `fcss` (functional CSS) classes are `single responsibility`,
they aren't at risk of overriding each other.
This almost eliminates the problems of the cascade
(changing a property somewhere won't break your code elsewhere).

Another extremely useful property you gain
from immutability is something called
**Referential Transparency**. In other words:
A thing does exactly what it says on the tin!

We know with a fair amount of confidence what
our button will look like just from reading the classes:

```html
<button class="pa2 br2 bg-green tc tracked">
```

but with `.btn` & `.btn-dwyl` classes, for all we know our button could look like:

![questionable](https://cloud.githubusercontent.com/assets/14013616/20143859/88f29ac8-a692-11e6-9980-012d3c5d1738.png)

Yikes! :open_mouth:

And what if we wanted to change it?
Do we change our "monolithic" button classes
and pray :pray: that they
don't break other buttons elsewhere? :boom:
On a BIG project?!

![lol](https://media1.giphy.com/media/sjfefACqq2BUc/200_s.gif)

Be realistic, we're likely to add more
and more classes to avoid this from happening.
This gets more and more wasteful over time,
adding bloat to our CSS files:

> In [the monolith] model, you will never stop writing css.
Refactoring css is hard and time consuming.
Deleting unused css is hard and time consuming.
And more often than not - it’s not work people
are excited to do. So what happens?
People keep writing more and more css -
[Adam Morse](http://mrmrs.github.io/writing/2016/03/24/scalable-css/).


## Why Tachyons?

What else does Tachyons specifically give us?

### Easy to Understand and Use

A great thing about tachyons is how quickly
and easily you can get up and running.
The classes are easy to understand
(once you get used to them),
If you know CSS, you know tachyons!

If you find the names too terse you can use the
[verbose version](https://github.com/tachyons-css/tachyons-display-verbose).


### _Mobile First_ Responsive Design

By far one of the most useful features is
that almost all classes have "responsive suffix" versions:

for example the "padding all 4" class
`pa4` also has 3 other versions:

```css
.pa4-ns { ... }
.pa4-m { ... }
.pa4-l { ... }
```

`ns`, `m`, and `l` are short
for "not small", "medium" and "large".

Tachyons gives you incredible flexibility
to change your design at different screen sizes.
And by default the "_non suffixed_"class
**is** the mobile class!
This encourages you to design for
***mobile first*** and expand outwards.
All of this without writing a line of css!
Tachyons has the referential transparency
of inline styles coupled with the power of media queries!

### Accessibility
Tachyons cares about accessibility!
Not only does the documentation actively encourage accessibility
by providing things like [accessible colour combinations](http://tachyons.io/docs/themes/skins/),
but whenever a release includes functionality that can cause
some accessibility issues, it comes with a :warning:
[warning to ensure everyone is aware](https://github.com/tachyons-css/tachyons/releases/tag/4.7.0)
of the appropriate usage. :heart:

> :warning: For quite some time people have been requesting an additional step in the type scale for 12px / .75rem. While 12px isn't readable for body copy it does have it's place in limited usage so I've added it to core. :warning:

### A Natural Workflow

Using Tachyon's styles in this way also seems
to encourage a more natural workflow when building UIs.

> Styles are localized at the HTML template level,
rather than being controlled by central CSS files.
This fits my workflow because I usually work
through a website's design one page at time... -
[Jason Li](http://notebook.hongkonggong.com/2016/04/21/is-tachyons-the-right-css-framework-for-me/)

Jason Li illustrates this perfectly:

![tachyonsexplanationbefore](https://cloud.githubusercontent.com/assets/14013616/20149566/caf62b80-a6a9-11e6-95a9-f06af3e8413f.png)
![tachyonsexplanationnow](https://cloud.githubusercontent.com/assets/14013616/20149576/d5bae650-a6a9-11e6-87b2-dcb65f1dc882.png)

### Works well with component based UIs

Using a templating engine or framework
(such as `Rails`, `React`, `Elm`, `Angular`)
means you can reduce the repetition of classes
in your html by reusing them as components.

### Great Performance that Scales

As your project grows larger, your stylesheet
doesn't (or only grows very minimally).
This has benefits for the user as there's
less CSS to download and the browser has
to register less styles overall
(it can cache the result of already computed styles).

> "Inline styles are 1 to 1 for the browser.
i.e an inline style can only style one element at a time.
While a class has a 1 to many relationship.
This has non-trivial deltas in rendering speed
and can greatly reduce jank in a complicated ui." -
[Adam Morse](https://github.com/tachyons-css/tachyons/issues/12)


## _How_?

### Try _Before_ You Commit (3 Easy Steps)

Getting started with Tachyons is as easy as 1, 2, 3!
We've created some examples for you to play around with
before you decide to use it on your own projects.

> If you want to see a quick-reference guide to Tachyons with detailed examples,
checkout our Clone of Bootstrap in Tachyons:
***Tachyons Bootstrap***: https://tachyons-bootstrap.dwyl.com

If you want to learn hands-on follow this tutorial
start by cloning and running it on your `localhost`.

#### 1. Clone this Repository

```sh
git clone https://github.com/dwyl/learn-tachyons.git && cd learn-tachyons
```

#### 2. Open one of the Example `.html` files in your web browser

![button example](https://cloud.githubusercontent.com/assets/194400/25722656/cc897900-310c-11e7-8915-bda326cf7dca.png)

See: `/examples`

#### 3. Edit Some Code!

In your Text Editor / IDE of choice,
edit one of the classes:

![button example red](https://cloud.githubusercontent.com/assets/194400/25722704/00d32c6a-310d-11e7-9065-1151a0d16e80.png)


#### _Optional_: Install "Live Server" for "_Live Reloading_"

If you prefer not to have to _manually_ refresh the page each time,
simply run the following command:

```
npm install && npm start
```
This will download the dependency on `live-server`
which will auto-open your `default` browser:

![button example blue](https://cloud.githubusercontent.com/assets/194400/25722773/43fbe298-310d-11e7-812e-54ec8efcb350.png)


e.g: http://localhost:8000/examples/buttons.html


### In your Own Project

You can get up and running by just
adding a link tag in your html

```html
<link rel="stylesheet" href="https://unpkg.com/tachyons@4.8.1/css/tachyons.min.css">
```

Or grab the latest version

```html
<link rel="stylesheet" href="https://unpkg.com/tachyons/css/tachyons.min.css">
```

If you want to _customize_ the styles you can
clone the tachyons repo locally and install the dependencies

```sh
$ git clone https://github.com/tachyons-css/tachyons.git
$ cd tachyons
$ npm install
```

Make the changes that you'd like to the css files and then run

```sh
$ npm run build
```

This will output both an _unminified_
and minified css file to the `/css` directory

Check out [this video](https://vimeo.com/174698456)
for a guide to setting up.

## Learning the ropes
The [Tachyons documentation](http://tachyons.io/docs/) is _fantastic_ as
reference material, incredibly well thought out, readable and easy to search
once you know what you want to do.

But if you just want to play around with tachyons and _get a feel for the
thinking behind it_, you'll find some well-used options below to get you started.

Once you start to get an understanding for how tachyons works,
we've found the [table of styles](http://tachyons.io/docs/table-of-styles/)
to be a very useful reference point.

### Responsive modifiers
Tachyons includes _modifiers_ which can be added onto the end of _any_ class
and will set up your media queries as shown [above](#mobile-first-responsive-design).

`ns` covers everything above mobile size, `m` covers roughly tablets, and `l`
covers roughly desktop sizes.

### Typography
The first place to start when designing is to set a [type scale](http://spencermortensen.com/articles/typographic-scale/)
so that you can _guarantee_ a harmonious progression of font sizes (from 'body
copy' to 'headlines') across your application or site - tachyons has this
**built in**!

Tachyons also [includes `.sans-serif` and `.serif`](http://tachyons.io/docs/typography/font-family/) which each have a set of
appropriate font family fallbacks.

#### [Font size](http://tachyons.io/docs/typography/scale/)
Aside from standard `f1` - `f6` sizes (`f7` was introduced in [tachyons 4.7.0](https://github.com/tachyons-css/tachyons/releases/tag/4.7.0),
but is not recommended for extensive use), `f-headline` and `f-subheadline` can
also be used for larger text requirements (usually for print).

#### [Line Height](http://tachyons.io/docs/typography/line-height/)
An agreeable line height promotes readability and tachyons offers 3 options
titled according to their most usual uses:
+ `lh-copy` with a line height of 1.5
+ `lh-title` with a line height of 1.25
+ `lh-solid` fixes line height to 1

#### [Font weight and style](http://tachyons.io/docs/typography/font-weight/)
Aside from `normal` and`b` for _bold_, `fw1` (corresponding to `font-weight: 100;`)
through to `fw9` (corresponding to `font-weight: 900;`) are available.

`i` can also be used for an italics font style.

#### [Text alignment](http://tachyons.io/docs/typography/text-align/)
`tl` aligns text left, `tc` centers it and `tr` aligns it to the right.

### Layout

Tachyons bases all of its [spacing on a specific ratio](http://tachyons.io/docs/layout/spacing/) that provides a much more
**effortless consistency in spacing across devices**, giving you a much higher
propensity for things to line up or to at least look harmonious.

#### [Padding and Margins](http://tachyons.io/docs/layout/spacing/)
Padding and margins both follow the same convention to create their 3 letter
classnames (e.g. `pa4` or `mb2`):
+ _First character:_ `p` or `m`: each classname starts with one of these to denote 'padding' or
'margin'
+ _Second character:_ `a` (all - adds padding or margin to top, bottom, left and right),
`h` (horizontal - adds padding or margin to left and right),
`v` (vertical - adds padding or margin to top and bottom),
`t` (top - adds padding or margin only to the top),
`r`  (right), `b` (bottom), `l` (left)
+ _Third character:_ a number from `0` to `7`

#### [Floating](http://tachyons.io/docs/layout/floats/)

Float left (`fl`), float right (`fr`) and float none (`fn`) are available and
sets elements to [block-level elements](https://developer.mozilla.org/en/docs/Web/HTML/Block-level_elements).

Because floats are removed from the flow of the page, remember that to force an
element to contain its floated children (i.e. the elements inside it), you'll
need to apply a [clearfix](http://tachyons.io/docs/layout/clearfix/) - in tachyons
you give the parent element the class `cf`.

#### [Display](http://tachyons.io/docs/layout/display/)
A simple set of classes that follow a similar naming convention to what should now be very familiar to you, e.g. `dib` for `{display : inline-block}` or `dn` for `{display: none}`.

There are also a set of display classes for table and table related display properties, which you can find in detail in the documentation with great examples.

#### [Widths](http://tachyons.io/docs/layout/widths/)
Widths are denoted by the `w` class, followed by one of 3 types of _modifiers_:
+ _Numbers scale_ which follows tachyons' powers of two scale mentioned above
  + Starting at `w1` (1rem) to `w5`(16rem)
  + e.g. `w1` sets the width of the element to the first step in the width
  scale (1rem) whereas `w4` sets the width to the fourth step (8rem)
+ _Percentage literals_
  + Starting at `w-10` for `10%` and going up in 10s (e.g. `w-20`, `w-30`, etc)
  until `w-100`
+ _Percentages_ (not supported in Opera mini or IE8 as these are calculations)
  + `w-third`, `w-two-thirds` and `w-auto`

**Max widths** are denoted by `mw` and support the _numbers scale_ above
(e.g. `mw-1` to `mw-10`) as well as `mw-100` (100%) or `mw-none`.

#### [Heights](http://tachyons.io/docs/layout/heights/)
Heights are denoted by the `h` class, followed by one of 3 types of _modifiers_:
+ _Numbers scale_ which follows tachyons' powers of two scale mentioned above
  + Starting at `h1` (1rem) to `h5`(16rem)
  + e.g. `h1` sets the height of the element to the first step in the
  height scale (1rem) whereas `h4` sets the height to the fourth step (8rem)
+ _Percentage literals_
  + Starting at `h-25` for `25%` and going up in 25s (e.g. `h-50`, etc) until `h-100`
+ _Values_
  + `auto` and `inherit`

#### [Position](http://tachyons.io/docs/layout/position/)
Elements are naturally statically positioned, but tachyons also support `.absolute` for absolute positioning and `.relative` for relative positioning.

For positioning of the elements, tachyons provides classes for
2rem, 1rem, 0, -1rem and -2rem, using the following format plus the number
(which can all be used with the media breakpoint modifiers at the end):
+ `top-` e.g. `top-0` (for `{top: 0}`) or `top-2`
+ `right-` e.g. `right--1` (for `{right: -1}`, note the additional dash here) or `right-1`
+ `bottom-` e.g. `bottom--2`
+ `left-` e.g. `left-1`

### Theming

Tachyons comes with a number of [pre-defined colours](http://tachyons.io/docs/themes/skins/) which you can use by themselves to denote _font_ colour or preface with `bg-` to give an element a _background_ colour (e.g. `bg-red`).

#### [Hovers](http://tachyons.io/docs/themes/hovers/)
There are quite a few hover states available, the basic being:
+ `dim` fades elements or text to 50% opacity on hover
+ `glow` brightens elements or text to 100% opacity on hover
+ `underline-hover` underlines elements or text on hover
+ `grow` makes elements scale by 5% of its size on hover

If you're looking for a specific effect, please read the _code_ at the bottom of the docs as there are more!

#### [Background size](http://tachyons.io/docs/themes/background-size/)
Background size allows an image to either:
+ fill its containing element (possibly showing only part of the image if it is bigger than the containing element)
using `cover`
+ be displayed in its entirety (possibly leaving a portion of the containing element blank if this is wider or taller than the image)
using `contain`

#### [Borders](http://tachyons.io/docs/themes/borders/)
Borders follow the same familiar pattern: `ba` for all 4 borders of the element, `bt` for the top border, `br` for the right border and so on.

The interesting part is that tachyons offers:
+ Border radius:
  + from `br0` (no radius) to `br5` (1rem)
  + `br-pill` to obtain a pill-shaped element
  + `br-100` for the 100% border radius to obtain a circular element
+ Border widths: from `bw1` (the thinnest) to `bw5` (the thickest)
+ Border styles (which can be combined with all other border properties):
  + `b--dashed`
  + `b--dotted`

#### [Opacity](http://tachyons.io/docs/themes/opacity/)
Opacity mostly follows a linear pattern `o-` with a number decrementing in multiples of 10: `o-90` (90% opacity), `o-80` (80% opacity) and so on.

In addition, tachyons offers: `o-05`, `o-025` and `o-0`.

## How To Create an Image Placeholder

Often in projects that feature images,
we want to display a _placeholder_ when no image is available.
For example in an e-commerce product, we don't want to have a "blank" `<div>`
because it's unfriendly to users.

We can _easily_ solve this issue with a bit of HTML and Tachyons:
```html
<div class="center bg-light-gray ba b--gray tc"
  style="width: 800px; height: 300px;">
  <img class="center pt5"/
  alt="Placeholder Image - Please upload an appropriate one."
  src="https://user-images.githubusercontent.com/194400/49571717-f392d480-f931-11e8-96f2-a8d10cfe375e.png">
  <p class="fw1">This is a placeholder image. <br />
    Please upload a more relevant one. Ideal dimensions:<br />
    <b class="fw5">Width: 800 pixels, Height: 300 pixels.</b>
  </p>
</div>
```
The effect is:
![image placeholder example](https://user-images.githubusercontent.com/194400/49573332-a57fd000-f935-11e8-9188-7f5a038a18b5.png)

Complete file for this example in:
[`image-placeholder.html`](https://github.com/dwyl/learn-tachyons/blob/master/image-placeholder.html)

### Break it down:

Let's break down this HTML and the Tachyons classes we have used:

+ A `<div>` which we use to "contain" (or "wrap") the image
and apply the grey background color:
  + `center` -  _center_ the `<div>` in the page,
  you can chose your own positioning to suit your needs.
  + `bg-light-gray` - literally background light gray.
  + `ba` - border "all" (_all sides of the div_)
  + `b--gray` - the color of the border, in this case `gray`.
  + `tc` - "text centre", these abreviations take a bit of learning,
  but once you know them they make perfect sense.
+ `<img>` a tiny placeholder image
with an appropriate `alt` text for accessibility.
  + `center` - same again, to center the image in the container `<div>`
  + `pt5` - "padding top 5", this is just to add some space.
+ `<p>` we use a paragraph to inform/remind the product owner
what the ideal dimensions are for the image they should upload.
  + `fw1` - "font weight 1", used to "fade" the font on the instructions.
  + `fw5` - "font weight 5", make the pixel dimensions more prominent.

To view this in action,
run
`npm start`
and visit:
http://127.0.0.1:8000/examples/image-placeholder.html


## Responsive Navigation Menu

Let's create a responsive navigation menu with _only_ HTML and CSS!

This is what you can expect in the desktop view:

![desktop-view-nav-menu](https://user-images.githubusercontent.com/194400/73554472-aa5de800-4443-11ea-941e-46c0d5c61337.png)

And this is what it looks like in a constrained (_mobile_) view:

![mobile-view-burger-nav-menu](https://user-images.githubusercontent.com/194400/73554480-ae8a0580-4443-11ea-9253-cf9d231c29c6.png)

The _expanded_ burger menu:

![mobile-view-burger-nav-menu](https://user-images.githubusercontent.com/194400/73554487-b2b62300-4443-11ea-981a-cf26e3818688.png)

This CSS-only (_no `JavaScript` required!_) responsive navigation menu
relies on [Isabel Castillo](https://github.com/isabelc)'s
brilliant _hidden_ `checkbox` idea:
https://isabelcastillo.com/pure-css-mobile-toggle-menu
(shared by @iteles in
  [github.com/dwyl/learn-tachyons/issues/10](https://github.com/dwyl/learn-tachyons/issues/10#issuecomment-304724294)❤️)

The _full_ code for creating a responsive nav is:

```HTML
<nav class="w-100 fixed top-0 bg-dark-gray">
  <!-- burger menu controlled by invisible checkbox -->
  <input type="checkbox" id="burger" class="dn">
  <label for="burger" class="dn-l fr pr5 f2">
    <i class="fa fa-bars white"></i>
  </label>
  <ul class="menu overflow-hidden db-l w-100-l w-70 list pa0 ma0 mt1-l pt1 f2 f3-l">
    <li class="fl pl5 pl6-l">
      <a href="/nav-menu.html">
        <img src="https://dwyl.com/img/favicon-32x32.png" alt="dwyl logo"/>
      </a>
    </li>
    <li class="di-l pl6 tl pt5-m pb2-m">
      <a href="#" class="white link">Portfolio</a>
    </li>
    <li class="pl5 pl6-m di-l tl pb2-m">
      <a href="#" class="white link">Blog</a>
    </li>
    <li class="pl5 pl6-m di-l tl pb2-m">
      <a href="#contact" id="contact-link" class="white link">Contact</a>
    </li>
    <li class="pl6-m tl dn-l pb3"> <!-- example of mobile-only menu item -->
      <a href="https://youtu.be/dQw4w9WgXcQ"
        class="white link">S'up?</a>
    </li>
  </ul>
</nav>

<!-- custom styles not available in taychons -->
<style>
  .menu {
    min-height: 2.8rem; /* no way to control min height in Tachyons */
    max-height: 0; /* hide menu completely when burger unchecked */
    transition: max-height 0.5s; /* show/hide menu transition */
  }
  /* when checkbox is checked, display menu (sibling element) */
  #burger:checked ~ .menu {
    max-height: 100%;
  }
</style>
```

Relevant to this quest is understanding the Tachyons display system:
https://tachyons.io/docs/layout/display
_Specifically_, understanding that
when the suffix `-m` is appended to a class
it means it only applies to the mobile view.
e.g: `pt5-m` means "_padding top level 5 mobile only_"
Likewise when the `-l` suffix is appended to a given class name,
it means the
e.g: `mt1-l` means "_margin top 1 only large screens_"

If you want to see this nav in action,
run `npm start`
and visit:
http://127.0.0.1:8000/examples/nav-menu.html


## Resources

+ [Tachyons.io](http://tachyons.io/)
+ [Tachyons Table of Styles](http://tachyons.io/docs/table-of-styles/) : http://tachyons.io/docs/table-of-styles/
+ [Tachyons Github Repo](https://github.com/tachyons-css/tachyons/) : https://github.com/tachyons-css/tachyons/
+ [Tachyons Verbose Version](https://github.com/tachyons-css/tachyons-display-verbose) : https://github.com/tachyons-css/tachyons-display-verbose
+ [Setting up Custom Tachyons Build](https://vimeo.com/174698456)
+ Tachyons Bootstrap Examples: https://tachyons-bootstrap.dwyl.com/
+ Cheat Sheet: https://roperzh.github.io/tachyons-cheatsheet

### Articles

+ [CSS and Scalability](http://mrmrs.github.io/writing/2016/03/24/scalable-css/)
+ [Functional Programming, CSS, and your Sanity](http://www.jon.gold/2015/07/functional-css/) : http://www.jon.gold/2015/07/functional-css/
+ [Rationalizing Functional CSS](https://marcelosomers.com/writing/rationalizing-functional-css/) : https://marcelosomers.com/writing/rationalizing-functional-css/
+ [Building and Shipping Functional CSS](https://blog.colepeters.com/building-and-shipping-functional-css/) : https://blog.colepeters.com/building-and-shipping-functional-css/
+ [Is Tachyons the right CSS framework for me?](http://notebook.hongkonggong.com/2016/04/21/is-tachyons-the-right-css-framework-for-me/) : http://notebook.hongkonggong.com/2016/04/21/is-tachyons-the-right-css-framework-for-me/
+ [FCSS](http://eng.wealthfront.com/2013/08/20/functional-css-fcss/) : http://eng.wealthfront.com/2013/08/20/functional-css-fcss/

### Questions and Discussions

+ [How is Tachyons different from inline styles?](https://github.com/tachyons-css/tachyons/issues/12) : https://github.com/tachyons-css/tachyons/issues/12
+ [What's so bad about inline css?](http://stackoverflow.com/questions/2612483/whats-so-bad-about-in-line-css) : http://stackoverflow.com/questions/2612483/whats-so-bad-about-in-line-css

### Future of Tachyons

Watch Adam Morse (_creator of Tachyons_)
describe the Future of Tachyons:

[![future-of-tachyons](https://cloud.githubusercontent.com/assets/194400/25709019/085b636c-30e0-11e7-9da4-6bb77a9b33d5.png)](https://youtu.be/XX47atVcVZE?t=1h1m11s "Future of Tachyons Talk @dwyl HQ - Click to Watch!") <br />
https://youtu.be/XX47atVcVZE?t=1h1m11s

<!--
### Does My App _Need_ To Be "_Beautiful_" for People to Use it?
-->
