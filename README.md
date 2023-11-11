## Fireship

The Fireship PRO course platform frontend is built with Svelte, Tailwind, Hugo, Firebase, & Flamethrower.

## Contributing

All static content is managed with Hugo in the `content` directory. You can easily fix typos by modifying the markdown directly on GitHub.

### How to Run it

First, install Hugo Extended version `0.101.0` or greater.

git clone <this-repo>
npm install
npm start

Check it on http://localhost:6969/.

## Developing Components 

Create a Svelte file in the `app/components` directory. It must have a custom element tag. 

<svelte:options tag="hi-mom" />

<script>
    export let greeting: string;
</script>

Hi Mom! {greeting}

Export the component from `app/main.ts`:

export * from './components/hi-mom.svelte';

Now use it anywhere in your HTML or Markdown. 

<hi-mom greeting="I made a web component"></hi-mom>

**Note:** A peculiar aspect of Svelte web components is that all styles must be encapsulated. You can use Tailwind, BUT only with `@apply` in the component. Global styles will not work.

## Commands

- npm start: Main dev server. Runs everything you need. 
- npm run dev: Runs components in isolation. Serves `app/index.html` as a playground for components. 
- npm run hugo: Only runs static site. 
- npm run build: Build for production.
