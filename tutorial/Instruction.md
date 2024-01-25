# Utility First Approach

## What is Utility First Approach?

Utility First Approach is a way of writing CSS where you write small, single purpose utility classes that can be combined to create complex styles.
This means that almost all different CSS attributes are written as classes, and then combined to create the desired style.

For example, instead of writing:

```css
.my-class {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}
```

You would write:

```css
.flex {
	display: flex;
}

.flex-column {
	flex-direction: column;
}

.justify-center {
	justify-content: center;
}
```

And then combine them in the HTML:

```html
<div class="flex-column flex justify-center"></div>
```

This is the approach that Tailwind CSS takes, and it is a very powerful way of writing CSS.
Tailwind already delivers all this utility classes, so you don't have to write them yourself.

It as well comes with some extra functionalities to create the views you want, like responsive classes, pseudo classes, etc.
We will see all of this in the next sections.

## Exercise

For the purpose to show this approach, we will rewrite the CSS of the small example [Card](./src/lib/Card.svelte) component in this project.

At the moment, the CSS is written in a more traditional way, with classes like `.card` and `.card-title`.
We will rewrite this CSS using Tailwind's utility classes.

For exmaple, instead of writing:

```css
.card {
	border: 1px solid #ccc;
	border-radius: 15px;
	margin: 24px;
	padding: 16px;
}
```

You would repalce the class card with following classes:

```html
<div class="m-6 rounded-lg border border-gray-300 p-4"></div>
```

You can find all the utility classes by searching in the [Tailwind CSS documentation](https://tailwindcss.com/docs).
Finish the exercise by rewriting the CSS of the [Card-Tailwind](./src/lib/Card-Tailwind.svelte) component using Tailwind's utility classes.

Compare the result with the [Card](./src/lib/Card.svelte) component.
