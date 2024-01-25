# Svelte TailwindCSS Tutorial

This tutorial will focuse on the use of tailwindcss.
Svelte is used as a framework for the tutorial.

Most of the svelte code will be given, the idea is to focus on the tailwindcss part.

### Prerequisites

- Node.js ~20.10.0
- yarn ~1.22.21

### Installation

```bash
yarn install
```

### Usage

```bash
yarn dev
```

## How does this tutorial work?

For each step of the tutorial, a branch is created.
The branch name is the topic handled and the step number, like this: `topic-stepNumber`.
For example, the branch `setup-1` is the first step of the setup topic.

Each of these branches are based on the previous step.
The instruction in the step are written in the file, [Instructions.md](tutorial/Insruction.md).
From their you will be guided trough the tutorial.

## Svelte Kit

This project is based on [Svelte Kit](https://kit.svelte.dev/).
I used it to have a quick setup for the tutorial.
With the comand:

```bash
npm create svelte@latest .
```

I created the base setup and added with the command:

```bash
npx svelte-add@latest tailwindcss
```

The tailwind to the project.
