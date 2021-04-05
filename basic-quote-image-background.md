<h1 class="capitalize">COMD2451</h1>
<h2 class="capitalize center">Creating a Basic Background Image Using CSS (and JS)</h2>

---

<section class="section">
	<h2 class="sentence">So how DOES one create a basic background image using CSS?</h2>

In **order** to **create** a ***basic*** `background-image` using `CSS`, one **uses** the [background-image property](https://www.w3schools.com/cssref/pr_background-image.asp).

The `background-image property` **sets** one or more `background-images` for an `element`.

By ***default***, the `background-image` is **placed** at the `top left corner` of an `element`, and **repeated** both `vertically` and `horizontally` if there is **space available** to do so.

The `background` of an `element` is the **total size** of the `element`, ***including*** `padding` and `border` (but ***not*** the `margin`).

One should ***always set*** a `background-color` as **fallback** in case if an `image` is ***not available***.

</section>

---

<section class="section">
	<h2 class="sentence">The background-image property: example 1</h2>

There are a **couple** of **ways** to ***add*** a `background-image` using `CSS`. ***One*** is to **set** the `background-image property` **targeting** the `body element`. **Something** like ***this***:

```css
body {
	background-image: url(/images/bryan-minear-317365.jpg);
	background-position: center center;
	background-repeat: no-repeat;
	background-size: cover;
	min-height: 100vh;
	overflow-x: hidden;
}
```

I **set** the `background-image property` to the **value** of `url(/images/bryan-minear-317365.jpg);`. The `path` I **use** here is the `absolute path` to the `image` in the **project folder**. ***However***, `locally` you **can use** a `relative path` if you like. It is ***better*** to **set** an `absolute path` and then **keep it** for **remote** (production site). On ***remote***, it **should be** an `absolute path`.

To **set** a `relative path`, I would ***do*** the ***following***:

```css
body {
	background-image: url(../images/bryan-minear-317365.jpg);
}
```

The `two dots`, `..`, means **stepping out** of the `current` (`styles`) `folder` and then ***into*** the `images folder` where the `image` ***resides***.

</section>

---

<section class="section">
	<h2 class="sentence">The background-position property and the background-image property</h2>

The [background-position property](https://www.w3schools.com/cssref/pr_background-position.asp) **sets** the `starting position` of a `background-image`.

By ***default***, a `background-image` is **placed** at the `top left` of an `element`, and **repeated** both `vertically` and `horizontally`. In the ***previous*** `background-image property` **example**, the ***following value*** was **set** on the `background-position property`:

```css
body {
	background-position: center center;
}
```

</section>

---

<section class="section">
	<h2 class="sentence">The background-repeat property and the background-image property</h2>

The [background-repeat property](https://www.w3schools.com/cssref/pr_background-repeat.asp) **sets** if/how a `background image` will be ***repeated***.

By ***default***, a `background-image` is **repeated** both `vertically` and `horizontally`.

The `background-image` is ***placed*** according to the `background-position property`. If ***no*** `background-position` is ***specified***, the `image` is **always placed** at the `element`'s `top left corner`. In the (***first***) `background-image property` **example**, the ***following value*** was **set** on the `background-repeat property`:

```css
body {
	background-repeat: no-repeat;
}
```

</section>

---

<section class="section">
	<h2 class="sentence">The background-size property and the background-image property</h2>

The [background-size property](https://www.w3schools.com/cssref/css3_pr_background-size.asp) ***specifies*** the `size` of the `background-image`.

There are ***four*** `different syntaxes` you can **use** with the `background-size property`:

+ the `keyword syntax` ("auto", "cover" and "contain"),

+ the `one-value syntax` (**sets** the `width` of the `image` (`height` ***becomes*** "auto"),

+ the `two-value syntax` (**first value**: `width` of the `image`, **second value**: `height`),

+ and the `multiple background syntax` (***separated*** with `comma`).

In the (***first***) `background-image` **example provided**, the `keyword syntax` with the `cover keyword` is **used**.

```css
body {
	background-size: cover;
}
```

***However***, in order to **truly cover** the ***available space*** vertically, I set the `min-height property` to `100vh`.

```css
body {
	min-height: 100vh;
}
```

The **value** of the `min-height` is `100vh`, which ***means*** that the `min-height` covers `100%` of the `viewport height`.

***Lastly***, I **set** the `overflow-x property` to the **value** of `hidden;`. This ***means*** that if the `width` of the `body element` **overflows** the `x axis` of the `viewport`, ***setting*** the **value** of `hidden` to the `overflow-x property` **hides** the **scrollbar** that ***appears*** when there is an **overflow** on the `x-axis`.

</section>

---

<section class="section">
	<h2 class="sentence">The background-image property using JavaScript</h2>

We ***don't*** have to always **set** a `background-image` to the `body element` of a **web page**. We can **set it** to ***another*** `element`. In the ***example below***, I **set it** to the `background` of a `article element` with the **class** of `.quote-cloud`. ***This time***, I **set** the `CSS styles` via `JavaScript`. The ***same*** can be **done** with ***plain*** `CSS`. **Set** with ***plain*** `CSS`, it would **look** like the ***following***:

```css
.quote-cloud {
	background-image: url(/images/alexander-stanishev-lT5QahSnruU-unsplash.jpg);
}
```

The ***drawback*** is that I can ***only set*** one `background-image`. I can **set** a ***number*** of `background-images` just in case if ***any previous*** `images` are ***not available***, but **those** are ***only fallbacks***.

***Using*** `JavaScript`, I can ***dynamically set*** multiple `background-images` with the ***click*** of the `section element` **containing** the **class** of `.quote-container`, ***dynamically changing*** the `background-image` of the `article element` with the class of `.quote-cloud` ***each time*** I ***click*** on the `section element`.

I can ***also set*** `CSS styles` via `JavaScript`. This is ***also known as*** `CSS` in `JS`.

This is the `JavaScript code` for **setting** the `background-image` for **example 2**:

```javascript
const quoteContainer = document.querySelector('.quote-container')

quoteCloud.style.backgroundImage = `url(${dir}${images[randomImage]})`
quoteCloud.style.backgroundPosition = 'center center'
quoteCloud.style.backgroundSize = 'cover'
quoteCloud.style.height = `100%`
quoteCloud.style.maxHeight = `600px`
quoteCloud.style.outline = `6px double #000`
```

I **use** the **HTML DOM** `style property` (this is the `property` which ***permits*** the **styling** of `elements` **using** `CSS` in `JavaScript`, and that is ***how*** one **sets styles** inside `JavaScript`.

I am also ***dynamically setting*** a `background-image` to the `article element` with the `.quote-cloud` **class**:

```javascript
quoteCloud.style.backgroundImage = `url(${dir}${images[randomImage]})`
```

The `quoteCloud` **variable** is `declared` and `initialized`. We ***declare*** the `variable` with the `const keyword`, and we ***initialize*** the `variable` by ***assigning*** it a **value** at the ***same time***.

**Using** a `template string literal` ***formed*** with **back ticks** `(``)`, I **set** the `url` of the `background-image` to ***dynamically*** be `images/` + a `random image` ***taken from*** a `const variable` called `images` with the **value** of an `array` of `images`.

What is an [array in JavaScript](https://www.w3schools.com/js/js_arrays.asp)? A `JavaScript array` is ***used*** to **store** `multiple values` in a ***single variable***.

An `array` can ***hold*** many values **under** a **single name** (the ***name*** of the `variable`), and you can ***access*** the **values** by **referring** to an `index number`.

We can ***create*** an `array` **using** an `array literal`. That ***means*** `defining` the **value** of the `variable` with ***opening*** and ***closing*** `square brackets`:

```javascript
const images = []
```

One ***doesn't*** have to ***initially*** stop there. One can ***do*** the ***following*** all **at once**:

```javascript
const images = [
	`burst-aoN3HWLbhdI-unsplash.jpg`,
	`cedric-vt-ILffJKYd1eA-unsplash.jpg`,
	`eberhard-grossgasteiger-y2azHvupCVo-unsplash.jpg`,
	`vincent-van-zalinge-vUNQaTtZeOo-unsplash.jpg`,
	`boxed-water-is-better-6aZp4_KfXT8-unsplash.jpg`,
	`daniel-roe-lpjb_UMOyx8-unsplash.jpg`,
	`boxed-water-is-better-km8IZ4xX9vA-unsplash.jpg`,
	`joshua-earle-ZMcLVBi9xx4-unsplash.jpg`,
	`caleb-jones-J3JMyXWQHXU-unsplash.jpg`,
	`alexander-stanishev-lT5QahSnruU-unsplash.jpg`,
	`sebastian-pichler-sblp4evk2gs-unsplash.jpg`
]
```

***Each*** `file name` within a `template string` ***represents*** the `name` of an `image file` with the `.jpg` **extension**. ***All*** these images **reside** within a **folder** called `images` within the `root` of my `Portfolio Site` **folder**, but ***because*** I **have** to ***separately add*** the `folder name` to the `image name` ***in order*** to **be able** to **render it** in the **browser**, I ***also*** have to `declare` and `initialize` a **variable** to the **value** of the `name` of the `directory`:

```javascript
/* absolute path represented by / before images/ */
const dir = `/images/`
```

***After*** I `declare` and `initialize` the **variable** called `dir`, I ***have*** to `declare` and `initialize` a `const variable` I call `quoteContainer`, which ***allows*** me to **access** and **manipulate** the `section element` with the **class** of `.quote-container` in the **browser**. It **looks** like ***this***:

```javascript
const quoteContainer = document.querySelector('.quote-container')
```

***Next***, I needed to **set** the `.addEventListener()` **method** on the `quoteContainer`. This `method` **sets up** a `function` that will be ***called*** whenever a **specified event** is ***delivered*** to the `target`. In ***our case*** here, the `.addEventListener()` **method** is ***attaching*** an `event handler` to a ***specified*** `element`, which is the `section element` with the **class** of `.quote-container`.

</section>

---

<section class="section">
	<h2 class="sentence">The section element .quote-container class and the .addEventListener() method</h2>

```javascript
/* randomize the index retrieval of the quotes array so that each time the user
clicks on the text rendered to the page, a random quote appears. In addition,
a random image appears at the same time, serving as a background for the quote.
And if no image appears (immediately at least), then a random background color
is generated and appears as the background of the quote instead. */
quoteContainer.addEventListener('click', () => {
	const articleHeading = document.querySelector('h2')
	const blockQuote = document.querySelector('blockquote')
	const quoteCloud = document.querySelector('.quote-cloud')
    const randomIndex = Math.floor(Math.random() * quotes.length)
	const randomImage = Math.floor(Math.random() * images.length)
    articleHeading.innerHTML = ``
	blockQuote.textContent = quotes[randomIndex]
	quoteCloud.style.backgroundImage = `url(${dir}${images[randomImage]})`
	quoteCloud.style.backgroundPosition = 'center center'
	quoteCloud.style.backgroundSize = 'cover'
	quoteCloud.style.height = `100%`
	quoteCloud.style.maxHeight = `600px`
	quoteCloud.style.outline = `6px double #000`
	setBg()
})
```

***Whenever*** a `user` **clicks** on the `section element` with the `.quote-container` **class**, the `block` of `code` ***between*** the **opening** and **closing curly braces** `{}` is ***executed***.

The `const variable` called `articleHeading`, **representing** the `h2 element` inside the `article element` with the **class** of `.quote-cloud`, is ***accessed*** using the `document.querySelector()` **method** so it can be ***manipulated***.

The `const variable` called `blockQuote`, ***representing*** the `blockquote element` inside the `article element` with the **class** of `.quote-cloud`, is ***accessed*** using the `document.querySelector()` **method** so it can be ***manipulated***.

The `const variable` called `quoteCloud`, **representing** the `article element` with the **class** of `.quote-cloud`, is ***accessed*** using the `document.querySelector()` **method** so it can be ***manipulated***.

The `const variable` called `randomIndex`, **representing** the `random index` of a `const variable` called `quotes`, is **used** to ***access*** a `quote` from a `quotes array`, which is the `value` of a `const variable` called `quotes`.

The `const variable` called `randomImage`, **representing** the `random index` of the `const variable` called `images` with the **value** of an `array` of `.jpg` **images**, is **used** to ***access*** an `image` to be **used** as the `background-image` of a `random quote` ***placed*** on **top** of the `image`.

The `articleHeading`'s `content` is ***cleared*** by **setting** the `.innerHTML` **JavaScript** `property` to an `empty template string`. If you ***recall***, by ***default***, the `articleHeading` **contains** the `text content` of `Click for quote!`. ***In order*** to **be able** to ***replace*** that `text` with the `text` of a `random quote` ***from*** the `quotes array`, we ***first*** have to **set** the `quoteCloud`'s `.innerHTML property` to the `empty template string`. ***Otherwise***, it would remain.

***Next***, I **set** the `.textContent property` on the `blockQuote` **variable** to the **value** of `quotes[randomIndex]`. `quotes` **represents** the `variable` **containing** the `array` of `.jpg images` as its **value**, and `[randomIndex]` **represents** a `random index` ***from*** the `quotes array`, **generated** with the `Math.floor(Math.random() * quotes.length)` **method**. The `Math.floor()` **method** `rounds down` a `number` ***containing*** `decimals` to its `largest integer`, ***less than*** or **equal to** the `number`.

**Example**:

```javascript
Math.floor(6.02)
// returns 6
```

The `Math.random()` **method** passed to the `Math.floor()` **method** `returns` a `random number` between `0` (**included**) and `1` (**excluded**). In ***other words***, it `always returns` a `number` which is ***less than*** `1`.

**Example using** `code` ***taken from*** the `body` of `quoteContainer.addEventListener()` **method**:

```javascript
Math.random() * quotes.length
```

`quotes.length` **represents** the `"length"` of the `quotes array`. In other words, the `number` of `quotes` **inside** the `quotes array`, ***each*** contained in `template strings`. In our `quotes array`, we have `11` **quotes**.

```javascript
const quotes = [
	`Dancing is silent poetry. - Simonides`,
    `It does not matter how slowly you go, so long as you do not stop. — Confucius`,
    `Wait a minute, wait a minute. You ain\'t heard nothin\' yet! - The Jazz Singer`,
    `One morning I shot an elephant in my pajamas. How he got in my pajamas, I don\'t know. - Animal Crackers`,
    `Do, or do not. There is no "try". - Star Wars: Empire Strikes Back`,
    `Once you eliminate the impossible, whatever remains, no matter how improbable, must be the truth. - Sherlock Holmes`,
    `I can write better than anybody who can write faster, and I can write faster than anybody who can write better. - A. J. Liebling`,
    `The significant problems we face cannot be solved at the same level of thinking we were at when we created them. - Albert Einstein`,
    `Everybody pities the weak. Jealousy you have to earn. - Arnold Schwarzenegger`,
    `Mother of mercy, is this the end of Rico? - Little Caesar`,
    `I have not failed. I've just found 10,000 ways that won't work. - Thomas Alba Edison`
]
```

`quotes.length` is **equal** to `11`. ***However***, we ***never*** start with the **number** `1` when ***counting*** the `number` of `items` in an `array`. We ***start with*** `0`. So `quotes[0]` would **represent** the ***first quote*** in the `array`, and `quotes[10]` would **represent** the `11`th **quote** in the `array`. ***Multiplying*** `quotes.length` by` Math.random()` will `return` a **number** between `0` and `10`, ***which is*** what **we want**!

</section>

---

<section class="section">
	<h2 class="sentence">The JavaScript .style property and the CSS background-image property</h2>

***Next***, I **set** the `.style property` to the `quoteCloud` variable **using** the ***camel-cased*** `backgroundImage property` to **set** a `random image` ***from*** the `images array` as a `background-image` to the ***randomly generated*** `quote` ***from*** the `quotes array`.

```javascript
/* randomize the index retrieval of the quotes array so that each time the user
clicks on the text rendered to the page, a random quote appears. In addition,
a random image appears at the same time, serving as a background for the quote.
And if no image appears (immediately at least), then a random background color
is generated and appears as the background of the quote instead. */
quoteContainer.addEventListener('click', () => {
	const articleHeading = document.querySelector('h2')
	const blockQuote = document.querySelector('blockquote')
	const quoteCloud = document.querySelector('.quote-cloud')
    const randomIndex = Math.floor(Math.random() * quotes.length)
	const randomImage = Math.floor(Math.random() * images.length)
    articleHeading.innerHTML = ``
	blockQuote.textContent = quotes[randomIndex]
	quoteCloud.style.backgroundImage = `url(${dir}${images[randomImage]})`
	quoteCloud.style.backgroundPosition = `center center`
	quoteCloud.style.backgroundSize = `cover`
	quoteCloud.style.height = `100%`
	quoteCloud.style.maxHeight = `600px`
	quoteCloud.style.outline = `6px double #000`
	setBg()
})
```

If we were ***simply using*** `CSS` to **set** 1 `background-image` to our `article element` with the **class** of `.quote-cloud`, we ***would do*** the ***following***:

```css
.quote-cloud {
	background-image: url("/images/boxed-water-is-better-6aZp4_KfXT8-unsplash.jpg");
}
```

And ***that*** would **be it**. We would then ***place*** `one quote` on **top** of ***this image***, and the `content` of the `article element` with the **class** of `.quote-cloud` would `"forever"` **remain** the ***same***.

***Instead***, we are **setting** the **JavaScript** `.style` **property** on the `quoteCloud` **variable** with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the ***camel-cased*** `backgroundImage property` to **set** a ***random*** `backgroundImage` ***from*** the `images array` **represented by** the `const variable` called `images`.

```javascript
quoteCloud.style.backgroundImage = `url(${dir}${images[randomImage]})`
```

</section>

---

<section class="section">
	<h2 class="sentence">The JS .style property and the CSS background-position property</h2>

***Next***, I **set** the **JavaScript** `.style` **property** to the `quoteCloud variable` **using** the ***camel-cased*** `backgroundPosition property` to **set** the `position` of the `background-image`.

If I ***were using*** `CSS` to **set** the `background-position` of the `image`, I would **have done** the ***following*** in my `external stylesheet`:

```css
.quote-cloud {
	background-position: center center;
}
```

***Instead***, we are **setting** the **JavaScript** `.style` **property** on the `quoteCloud` **variable** with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the ***camel-cased*** `backgroundPosition property` to **set** the `background-position` of the `image`.

```javascript
quoteCloud.style.backgroundPosition = `center center`
```

I **use** a `template string literal` to **wrap around** the **value** of `quoteCloud.style.backgroundPosition`, but I ***also*** could have used `single` or `double quotes`. One just **has** to be ***consistent*** when **using** `single` or `double quotes`. It's **industry convention** and **standard** to keep things ***stylistically consistent***.

</section>

---

<section class="section">
	<h2 class="sentence">The JS .style property and the CSS background-size property</h2>

***Next***, I **set** the **JavaScript** `.style` **property** to the `quoteCloud variable` **using** the ***camel-cased*** `backgroundSize property` to **set** the `size` of the `background-image`.

If I ***were using*** `CSS` to **set** the `background-size` of the `image`, I would ***have done*** the ***following*** in my `external stylesheet`:

```css
.quote-cloud {
	background-size: cover;
}
```

***Instead***, we are **setting** the **JavaScript** `.style` **property** on the `quoteCloud variable` with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the ***camel-cased*** `backgroundSize property` to **set** the `background-size` of the `image`.

```javascript
quoteCloud.style.backgroundSize = `cover`
```

***Next***, I **set** the **JavaScript** `.style` **property** on the `quoteCloud variable` with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the `height property` to **set** the `fluid height` of the `article element` with the **class** of `"quote-cloud"`.

If I ***were using*** `CSS` to **set** the `height` of the `article element` with the **class** of `.quote-cloud`, I would ***have done*** the ***following*** in my `external stylesheet`:

```css
.quote-cloud {
	height: 100%;
}
```

***Instead***, we are **setting** the **JavaScript** `.style` **property** on the `quoteCloud variable` with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the `height property` to **set** the `height` of the `article element` with the **class** of `quote-cloud`.

```javascript
quoteCloud.style.height = `100%`
```

***Next***, I **set** the **JavaScript** `.style` **property** on the `quoteCloud variable` with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the ***camel-cased*** `maxHeight property` to **set** the ***maximum*** `height permissible` of the `article element` with the **class** of `.quote-cloud`.

If I ***were using*** `CSS` to **set** the `max-height` of the `article element` with the **class** of `.quote-cloud`, I would ***have done*** the ***following*** in my `external stylesheet`:

```css
.quote-cloud {
	max-height: 600px;
}
```

***Instead***, we are **setting** the **JavaScript** `.style` **property** on the `quoteCloud variable` with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the ***camel-cased*** `maxHeight property` to **set** the ***maximum*** `height permissible` for the `article element` with the **class** of `.quote-cloud`.

```javascript
quoteCloud.style.maxHeight = `600px`
```

***Last*** of ***all***, I **set** the **JavaScript** `.style` **property** on the `quoteCloud variable` with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the `outline property` to **set** a `double border` **right outside** of the `article element` with the **class** of `"quote-cloud"` in the `HTML markup`, to **set** a `double outline` that is ***drawn around*** the `article element`, ***outside*** the ***borders***, instead of the ***inside edges***, to **make** the `element` `"stand out"`.

if I ***were using*** `CSS` to **set** the (`double`) `outline` of the `article element` with the **class** of `.quote-cloud`, I would ***have done*** the ***following*** in my `external stylesheet`:

```css
.quote-cloud {
	outline: 6px double #000;
}
```

***Instead***, we are **setting** the **JavaScript** `.style` **property** on the `quoteCloud variable` with the **class** of `"quote-cloud"` in the `HTML markup`, and **using** the `outline property` to **set** a `double outline` ***drawn around*** the `article element`, ***outside*** the ***borders***, **instead of** the ***inside edges***, to **make** the `element` `"stand out"`.

```javascript
quoteCloud.style.outline = `6px double #000`
```

</section>

---

<section class="section">
	<h2 class="sentence">Setting a dynamic background-color to the article element as a fallback</h2>

At the ***end*** of the `code block` **inside** the `quoteContainer.addEventListener()` **method** is a `setBg()` function call. This is a `call` to a `function expression` ***created by*** the `declaration` and `initialization` of a `const variable` called `setBg`. It ***looks*** like the ***following***:

```javascript
const setBg = () => {
	const body = document.querySelector('body')
	const quoteCloud = document.querySelector('.quote-cloud')
	const randomColor = Math.floor(Math.random()*16777215).toString(16).padStart(6, '0')
	quoteCloud.style.backgroundColor = `#${randomColor}`
	console.log(`#${randomColor}`)
	body.style.backgroundColor = `#${randomColor}`
}
```

When the `setBg` function expression is ***called***, `setBg()`, ***all*** the `code` **inside** its `code block`, ***defined*** by an **opening** and **closing curly brace** `{}`, is ***executed***. Let's ***break*** this ***down***.

***First***, I `declare` and `initialize` a `const variable` called `body`. It ***accesses*** the `body element` in the `HTML markup` **using** the `document.querySelector()` **method**, so that the `body element` can be ***manipulated*** with `JavaScript`.

***Next***, I `declare` and `initialize` a `const variable` called `quoteCloud`. It ***accesses*** the `article element` with the **class** of `.quote-cloud` in the `HTML markup` using the `document.querySelector()` **method**, so that the `article element` with the **class** of `.quote-cloud` can be ***manipulated*** using `JavaScript`.

***Next***, I `declare` and `initialize` a `const variable` called `randomColor`. We **multiply** `Math.random()*16777215` because there are [16777216 possible RGB color variations](https://stackoverflow.com/questions/1484506/random-color-generator/25821830#25821830), and we want to ***potentially*** be able to **render** any one of ***them***. ***However***, we **can't use** the **number** `16777216`, because we **have** to `count` from `0`, ***similar*** to `counting` the `number` of `items` in an `array`. ***Instead***, we **use** `16777215`.

I **set** the `.toString()` **method** on `Math.floor(Math.random()*16777215)`, ***passing it*** the **number** `16`, `.toString(16)`, because this ***creates*** a `hexadecimal value` for us. But we ***also*** have to **chain** the `ES6` (`Modern JavaScript` ***introduced*** in `2015`) `.padStart(6, '0')` **method** to ***ensure*** that the `hexadecimal value` ***always contains*** `6 characters`. The `6` **passed** to `.padStart()` **stands for** the `six places` for the `six characters`, and the `'0'` **stands for** the `value` ***used*** to **pad** the `hexadecimal value` to `6 characters`. The `.padStart(6, '0')` **method** simply ***ensures*** that a `hex color code` **containing** six characters is ***always generated***, because by ***default***, that is ***not*** always the case. It's just **one** of **those** `"JavaScript anomalies"`!

***Next***, I **set** the **JavaScript** `.style property` on the `quoteCloud variable` with the **class** of `.quote-cloud`, using the `backgroundColor property` to **set** the ***fallback*** `background-color` of the `article element` with the **class** of `.quote-cloud`. I **use** a `#` ***followed by*** `template interpolation` of the `randomColor variable` to ***dynamically set*** a `hexadecimal color code` as the **value** of the `backgroundColor property`.

I ***do*** the ***same*** when ***dynamically setting*** the `backgroundColor` of the `body element` via the `const variable` called `body`.

Then I ***call*** the `setBg()` function at the **end** of the `code block` of the `quoteContainer.addEventListener()` **method**.

```javascript
/* randomize the index retrieval of the quotes array so that each time the user
clicks on the text rendered to the page, a random quote appears. In addition,
a random image appears at the same time, serving as a background for the quote.
And if no image appears (immediately at least), then a random background color
is generated and appears as the background of the quote instead. */
quoteContainer.addEventListener('click', () => {
	const articleHeading = document.querySelector('h2')
	const blockQuote = document.querySelector('blockquote')
	const quoteCloud = document.querySelector('.quote-cloud')
    const randomIndex = Math.floor(Math.random() * quotes.length)
	const randomImage = Math.floor(Math.random() * images.length)
    articleHeading.innerHTML = ``
	blockQuote.textContent = quotes[randomIndex]
	quoteCloud.style.backgroundImage = `url(${dir}${images[randomImage]})`
	quoteCloud.style.backgroundPosition = 'center center'
	quoteCloud.style.backgroundSize = 'cover'
	quoteCloud.style.height = `100%`
	quoteCloud.style.maxHeight = `600px`
	quoteCloud.style.outline = `6px double #000`
	setBg()
})
```

</section>

---

<section class="section">
	<h2 class="sentence">Quote cloud related CSS inside the external stylesheet</h2>

I **set** `CSS` in `JS` that is ***related specifically*** to the `background-image` of the `article element` with the **class** of `.quote-cloud`. As for the **placement** and **styling** of the `blockquote element`, and other ***more general*** `styling` which did ***not*** have to be **applied** via `JavaScript`, I `defined` ***those styles*** inside my `external stylesheet`:

```css
/* Section quote container styling */
.quote-container {
	cursor: pointer;
	display: flex;
    align-items: center;
	flex-direction: column;
	font-family: 'Barlow', sans-serif;
	height: 50vh;
	justify-content: center;
	margin: 3rem auto;
    margin: 12vh auto;
    max-width: 800px;
    width: 90%;
}

/* article quote-cloud styling desktop */

.quote-cloud {
	cursor: pointer;
	display: flex;
	align-items: center;
	flex-direction: column;
	justify-content: center;
	margin: 0.5rem;
	text-align: center;
	width: 90%;
}

.quote-cloud h2 {
	font-weight: normal;
}

.quote-cloud blockquote {
	color: #fff3f3;
	margin: 0 auto;
	text-shadow: 1px 2px 2px #000;
	width: 90%;
}

/* end article quote-cloud styling desktop */

/* font-size specific max-width: 640px and max-height: 360px (Microsoft Lumia 550) */

@media (width: 640px) and (height: 360px) {
	h1 {
		margin-top: 0;
	}
}

/* end font-size specific max-width: 640px and max-height: 360px (Microsoft Lumia 550) */

/* font-size styling h1, h2, blockquote media query min-width: 600px */
@media (min-width: 600px) {

	h1 {
		font-size: 3.5rem;
	}

	h2 {
		font-size: 2.5rem;
	}

    blockquote {
        font-size: 2rem;
	}
}

/* End media query smaller screens for section and article elements in index.html */

```

</section>

---

<section class="section">
	<h2 class="sentence">Related Resources</h2>

+ [Random color generator: stackoverflow](https://stackoverflow.com/questions/1484506/random-color-generator/25821830#25821830)

+ [Random Hex Color Code Generator in JavaScript: Paul Irish](https://www.paulirish.com/2009/random-hex-color-code-snippets/)

+ [Generating random color with single line of js code: dev.to](https://dev.to/akhil_001/generating-random-color-with-single-line-of-js-code-fhj)

+ [CSS background-image Property: w3schools](https://www.w3schools.com/cssref/pr_background-image.asp)

+ [Creating a Background Image with the Body Element: Maria D. Campbell](https://github.com/interglobalmedia/basic-quote-body-image-background/blob/master/basic-quote-body-image-background.md)

</section>
