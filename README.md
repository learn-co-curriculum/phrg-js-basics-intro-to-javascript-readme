# Intro to JavaScript

## Objectives
- Describe the JavaScript language and its many uses in general terms.
- Talk about the various versions of JavaScript (_ES5_, _ES2015_, and so on).
- Use the console in the Chrome dev tools to write some JavaScript code.
- Understand the importance of coding along with every example. Practice, practice, practice!

## Introduction
_JavaScript_, commonly abbreviated as _JS_, is the programming language of the web. Along with HTML and CSS, it's used to create everything from Google to Facebook to Wikipedia to Amazon to Netflix.

When you look at the content on a website, each of the three main web technologies plays a role:
- HyperText Markup Language (HTML) provides structure to the content, arranging it in a nested, tree-like manner.
- Cascading Style Sheets (CSS) adds styling to the page, letting us customize the look of text content, the background color of the page, and the size and position of the various HTML elements.
- JavaScript does **pretty much everything else**.

When you hover your mouse over a button and it wiggles in anticipation, that's JavaScript.

When you see new notification alerts on Twitter without refreshing the page, that's JavaScript.

When new content progressively appears at the bottom of the page as you scroll down your Facebook news feed, that's JavaScript.

## A brief history lesson
In 1995, a Netscape developer named Brendan Eich created JavaScript in **ten days**. For a point of comparison, Rich Hickey spent about **two-and-a-half years** working on a language called _Clojure_ before he released it to the public.

So the first version of the language was built incredibly quickly. There were a few other competitors vying to become the language of the web, but they never gained enough traction to knock off JavaScript. And then... not much happened. For **years**.

There were incremental improvements and adjustments, but JavaScript development around 2000 very much resembled JavaScript development in the mid-1990s. And then _Outlook Web Access_ ("OWA") happened.

Around the turn of the century, Microsoft wanted to give its customers a way to access their email via a web browser (in addition to the standalone Outlook application). They quietly added a new JavaScript feature to Internet Explorer that allowed an already-loaded web page to fire off a request for additional data. This would allow OWA to periodically check for new email in the background **without reloading the page**. It was a huge improvement over existing webmail services that required the whole page to be reloaded in order to check for new email.

The feature was later standardized as `XMLHttpRequest`, and the process of making requests for additional data became known as _Asynchronous JavaScript and XML_, or _AJAX_. We'll take a long look at AJAX later on in the JavaScript material. By the time Gmail came along in 2004 with its heavy dependence on AJAX, JavaScript was in the early stages of a meteoric rise in popularity and usefulness that has continued up through the present day.

### Standardization and modernization
However, even though AJAX provided a lot of useful functionality to the language, it was still a nightmare to program in. Different browsers implemented different features in different ways. Getting your code to work the same in every browser was virtually impossible. There were a few competing camps who all had different ideas about what the language should be, and standardization seemed out of the question. Then, in early 2009, the adversaries came together to iron out their differences and agree on a common set of goals. In late 2009, the fifth version of JavaScript was released. It's known as **ES5** ('ES' for **ECMAScript**, the official name of the JavaScript specification) or **Harmony** (because it harmonized competing implementations of the ECMAScript specification).

Harmonization was great, but the language was still a bit lacking on modern language features. The JavaScript overlords began to address those concerns in 2015 with the unveiling of **ES6**, the sixth version of JavaScript. They also decided to start releasing updates every year to encourage more active development of the language, so **ES6** is better known as **ES2015**. Since then, they've released **ES2016** and **ES2017**, both of which have brought additional modern features into the language.

## No compiler? No problem!
The name _JavaScript_ was chosen as a marketing ploy: the _Java_ language was all the rage in 1995. The two languages share very little in common. Some JS syntax is borrowed from Java (to make it more familiar for those early developers coming over from the world of Java), but that's about it.

Unlike Java, JavaScript code doesn't need to be compiled. **The code that you write in a JavaScript file is the exact same code that the web browser parses and runs**. In a compiled language like Java, you write some code in a human-readable format, and then the compiler takes that code and essentially translates it into machine-readable code. That means that it's very difficult to open up the source code for an application written in a compiled language and poke around it to understand what's going on.

Because it doesn't get compiled, that is **exactly what we can do with JavaScript code**. Towards the end of this JavaScript curriculum, you'll find yourself able to go to a website you like, open up the source code using your browser's developer tools, and **look directly at all of the JavaScript code used on that site**. This is an extremely powerful feature of the language and an incredible tool for learning by example.

## Using the developer tools
Every major browser comes with a built-in set of developer tools that you can use to inspect, modify, and debug the content of a web page.

***NOTE***: To ensure that instructions and screenshots match up with your experience, we recommend using the [Google Chrome](https://www.google.com/chrome/index.html) browser.

To [open the dev tools in Chrome](https://developers.google.com/web/tools/chrome-devtools/console/#open_as_panel
), press `Ctrl+Shift+J` (Windows / Linux) or `Cmd+Opt+J` (Mac). Chrome ships with a whole suite of useful dev tools, but the only one we care about for now is the JavaScript console.

The console is a sandboxed environment in the browser where we can type and run arbitrary JavaScript code. Once we start declaring variables and functions in separate JavaScript files, we'll be able to access and play around with them in the console. The console is the single best tool for debugging JavaScript in the browser, so start familiarizing yourself with it now.

The `Ctrl+Shift+J` / `Cmd+Opt+J` command should open up straight into the console. If, for whatever reason, it doesn't, you can always click on `Console` in the dropdown (when the dev tools are collapsed) or in the list of tabs:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.gif" alt="Opening the console">
</picture>

To access the Chrome dev tools settings — for example, to change the theme from light to dark — click the three vertical dots:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.gif" alt="Changing the theme">
</picture>

If at any point the console becomes cluttered with errors, warnings, or anything else, click the `Clear console` button:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.gif" alt="Clearing the console">
</picture>

Okay, okay, enough background and setup. Let's write some code!

## Writing your first JavaScript code
We'll start off with some simple math. In the console, type `1 + 1` and press enter. You should see the number `2` appear. You just wrote and ran your first line of JavaScript code!

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/celebration.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/celebration.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/celebration.gif" alt="Celebration time!">
</picture>

The code you wrote, `1 + 1` is an _expression_. In JavaScript, an expression is **[a valid unit of code that returns a value](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Expressions)**. The value that it returned, `2`, is aptly referred to as the **return value** of the expression. Try out some more mathematical expressions and see what they return!

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.gif" alt="Math in the console">
</picture>

Next up, let's write some text. To make sure the JavaScript engine knows that we're trying to write some literal text, we need to wrap it in quotation marks, like so:
```js
"This is some literal text in JavaScript!"
```

Go ahead and type that classic phrase, `"Hello, world!"`, into the console and press enter. It returned `"Hello, world!"` right back to us! Try typing some more literal text into the console, such as your name. Don't forget the quotation marks!

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/text_in_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/text_in_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/text_in_console.gif" alt="Text in the console">
</picture>

## Built-in goodies
JavaScript comes with a number of built-in goodies that can help us build and debug our applications. One of the simplest is the `alert()` function, which creates a simple alert in the browser window:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/alerting_in_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/alerting_in_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/alerting_in_console.gif" alt="Alerting in the console">
</picture>

Try it out yourself! Put some numbers, text, or maybe even a mathematical equation between `alert()`'s parentheses and see what happens.

This is just a quick demonstration of one of the many features JavaScript makes available to you in the browser. In the lessons to come, we'll learn a lot more about the built-in magic JavaScript provides for us.

## Syntax and semicolons
A quick note on syntax. In JavaScript, ending each statement with a semicolon is optional. When you run some JavaScript code in the browser, the JavaScript engine actually makes multiple passes over the same code. The first pass is to parse the syntax of your code. The second pass is to initialize variables and functions and store them in memory. And the third pass is to actually execute the code line-by-line. We'll learn more about the second and third phases in an upcoming lesson.

During the first pass as it's parsing the syntax of your JavaScript file, the engine undertakes a process called _automatic semicolon insertion_. The name says it all, and this is why statement-ending semicolons are optional — the JavaScript engine will automatically insert them for us. There's one main gotcha that we'll talk about in the lesson introducing functions, but it generally works as expected. That being said, semicolons **are** part of the JavaScript syntax, whether you insert them or the engine does. It's not a bad idea to practice putting them at the end of your statements, at least until you become more comfortable with the overall syntax of the language. Many of the examples in upcoming lessons will include semicolons to show you where they go.

### Referencing functions, keywords, and variables
Throughout the JavaScript curriculum on Learn.co, we'll often refer to pieces of code in these READMEs. If the piece of code is a function, we'll include a pair of trailing parentheses to mark it as such, e.g., `myFunction()` or the already introduced `alert()`. If the piece of code is a keyword in the language or a variable that we're referencing, there'll be no parentheses: `myVariable`, `debugger`, `if...else`, etc.

## Your mission, should you choose to accept it
<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/mission_impossible.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/mission_impossible.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/mission_impossible.gif" alt="Mission: Impossible">
</picture>

It's impossible to overstate how important practice is when you're learning a new programming language. You can read the READMEs and watch the videos, but the true education is in writing code — **lots** of it.

As you move through the JavaScript curriculum, you should almost always have a browser console open, either on the lesson page or in a separate window. Code along with every example. Get used to the syntax and familiarize yourself with the errors that arise when you mistype something. Clear the console or simply refresh the page whenever you need a clean slate. Code, code, **code**, **code**, ***code***.

## Wrapping up
JavaScript is by now one of the most popular languages in the world, and it shows no signs of slowing up. It's still the only programming language that can run in every major browser (HTML is a _markup language_ and CSS is a _style sheet language_), and the advent of [Node.js](https://nodejs.org/en/about/) in 2009 brought server-side JavaScript to the masses.

A language of many talents, JavaScript allows us to create incredibly diverse applications that run in the browser, on the server, on the desktop, and on mobile devices. It's a flexible language, allowing us to program in many different styles — functional and object-oriented, in particular — mixing and matching concepts to adapt to our needs. It's powerful, scalable, and has a robust community of developers churning out new code and advancing the language. And, finally, it's a great first or second language to learn.

While not **quite** as developer-friendly and idiomatic as Ruby, JavaScript is lenient in a lot of ways that will make your life easier. It's dynamically typed, so, for example, you can store different types of data in the same variable without the language freaking out. JavaScript also doesn't care about whitespace, so you can indent and space out your code to your heart's content — make it look pretty! And, as we'll see in the upcoming lessons, JavaScript will bend over backwards to do what you ask it to instead of chucking errors left and right.

This curriculum will provide the fundamental tools to unlock the power of JavaScript and take the next step on your journey to becoming a full-stack web developer.

Are you excited yet?! Your JavaScript journey is about to begin!

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/get_pumped.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/get_pumped.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/get_pumped.gif" alt="Get pumped!">
</picture>

## Resources
- [W3C — A Short History of JavaScript](https://www.w3.org/community/webed/wiki/A_Short_History_of_JavaScript)
- [Wikipedia — ECMAScript: Versions](https://en.wikipedia.org/wiki/ECMAScript#Versions)

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/js-basics-intro-to-javascript-readme' title='Intro to JavaScript'>Intro to JavaScript</a> on Learn.co and start learning to code for free.</p>
