# CSS States

One of the most important things to understand about CSS is that it is a state-based language.
This means that the way an element looks is determined by its current state. For example, a button can be in a default state, a hover state, a pressed state, a disabled state, and so on.
Each of these states can have different styles applied to it.

With old fashioned CSS, you would have to write a separate CSS rule for each state. For example:

```css
button {
	background-color: blue;
}

button:hover {
	background-color: red;
}

button:active {
	background-color: green;
}

button:disabled {
	background-color: gray;
}
```

In Tailwind, you can use the `hover`, `focus`, `active`, and `disabled` variants to apply different styles to an element based on its state.

```html
<button class="bg-blue-500 hover:bg-red-500 active:bg-green-500 disabled:bg-gray-500">
	Click me
</button>
```

This keeps the amount of code smaller, but the length of the class will explode over time.
What is one downside of tailwind.

## Exercise

1. Create a new component called `Button` in `src/lib/Button.svelte`
2. Add different state for the button
   a. hover
   b. focus
   c. active
   d. disabled
3. Add this button to the card component

## Solution

Can be found in the branch `concept_CSS-State-1-solution`
