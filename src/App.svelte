<script lang="ts">
  import logo from './assets/svelte.png'
  import Counter from './lib/Counter.svelte'
  import { count } from './state/counter.js';
  import List from './lib/List.svelte';

  let countValue;

  count.subscribe(value => {
    countValue = value;
  });
</script>

<main>
  <h1>The count is {countValue}</h1>
  <Counter />

  <hr>

  <List />
</main>

<style>
  @import "styles/button.css";

  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
