<script lang="ts">
  import "./App.css";
  import { onMount } from "svelte";
  import Footer from "./components/Footer.svelte";
  import Quotes from "./Data/Quotes";
  import TheQuote from "./components/TheQuote.svelte";

  let point: number = Math.floor(Math.random() * Quotes.length);

  onMount(() => {
    randomQuote();
  });

  function randomQuote() {
    point = Math.floor(Math.random() * Quotes.length);
  }
</script>

<main class="main-screen">
  <div class="text-lg">Life coach quotes</div>
  <TheQuote quote={Quotes[point].quote} coach={Quotes[point].coach} />
  <button class="btn-green" title="click to random quote" on:click={randomQuote}>Random Quote</button>
</main>
<Footer />
