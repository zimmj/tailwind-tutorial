# Understanding of the Setup of Tailwind CSS

## What is Tailwind CSS?

In short: Tailwind is a utility-first CSS framework. It moves all CSS to pre-defined classes. This makes it easy to use and to customize.
For more information, see the [Tailwind CSS documentation](https://tailwindcss.com/docs).

## How does Tailwind CSS work?

The main magic happens in the postcss.config.js file. There we tell svelte kit to run tailwindcss to figure out which classes are used in the project.
All used classes are then written into the app.css file.
This file is loaded globally in the index.html file.
Therefore, all classes are available in the project.

Trough the purging of not used classes, the app.css file is kept small.
But you can not easily add classes in the browser to test them out.
They might not exist in the currect css file.

## Try out the tailwind css

To try if tailwind is working, we cann add some simple classes to the index.html file.
For example, we can add the class `text-red-500` to the div tag.

As we see the text is now red.
