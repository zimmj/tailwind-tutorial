# CSS States

The nice thing about tailwind is that they created modifier for the different things you can imagine in CSS.

The most common ones are:

- [pseudo-classes](https://tailwindcss.com/docs/hover-focus-and-other-states#pseudo-classes)
- [pseudo-elements](https://tailwindcss.com/docs/hover-focus-and-other-states#pseudo-elements)
- [media and feature queries](https://tailwindcss.com/docs/hover-focus-and-other-states#media-and-feature-queries)
- [attribute selectors](https://tailwindcss.com/docs/hover-focus-and-other-states#attribute-selectors)

and event [custom modifiers](https://tailwindcss.com/docs/hover-focus-and-other-states#custom-modifiers)!

With all of them, we can build a rich and responsive UI.

## Pseudo-classes

We already saw the `hover` pseudo-class and simmilar state clasess in the previouse branch.
But there are more of them I like to show and talk about.
One of the interesting ones are the place pseude classes:

- first
- last
- odd
- even

They are very useful when you want to style a list of items.
For example, if you want padding on the first and last element.

```html
<ul role="list" class="divide-y divide-slate-200 border p-6">
	{#each users as user}
	<li class="flex py-4 first:pt-0 last:pb-0">
		<div class="ml-3 overflow-hidden">
			<p class="truncate text-sm font-medium text-slate-500">{user.name}</p>
			<p class="truncate text-sm text-slate-500">{user.email}</p>
		</div>
	</li>
	{/each}
</ul>
```

This code you can see in the [simple list](./src/lib/SimpleList.svelte) component.

As a samll exercise, try to add a background color to the odd and even elements.
Like in a old fashion table.

For a complete list of pseudo-classes, check out the [tailwind documentation](https://tailwindcss.com/docs/hover-focus-and-other-states#pseudo-classes).

### Styling with groups, peers, siblins and descendants

Another powerful feature of tailwind is the ability to style elements based on their relation to other elements.
This allow us to create complex UIs with a few lines of code and no need for extra JS.
As we can listen to the state of another element.

The syntax is very simple, we just need to add the `group` class to the parent element and then we can use the `group-hover` pseudo-class to style the children.

```html
<div class="group">
	<button class="rounded bg-blue-500 px-4 py-2 font-bold text-white hover:bg-blue-700">
		Grouped Button 1
	</button>
	<button
		class="rounded bg-blue-500 px-4 py-2 font-bold text-white hover:bg-blue-700 group-hover:hidden"
	>
		Grouped Button 2
	</button>
</div>
```

In this example, we have two buttons, but only one is disapearing when we hover over the parent.

You can name the group with the syntax: `group/{name}`. With this you can work with multiple groups in the same component.

The other based classes are:

- `peer`: elements that share the same parent
- `sibling`: elements that share the same parent and sibling is defined before it is used
- `has`: elements that have a child with a specific class or state

You can see the exmplae int the [Group-Example](./src/lib/GroupExample.svelte) component.
You can remove the class invisble from the div in +page.svelte to see the component.

As an exercise:

- Create a component with a button, that shows a dropdown when clicked.
- The element in the dropdown should indicate when when they have a link in them.
- The element should change color when hovered.
- The whole dropdown should change apperane when something is selected.
