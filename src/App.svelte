<script lang="ts">
  import './App.css'
  import { onMount } from "svelte";
  import Footer from "./components/Footer.svelte";
  import Quotes from "./Data/Quotes";

  let point: number = Math.floor(Math.random() * Quotes.length);

  onMount(() => {
    randomQuote();
  });

  function randomQuote() {
    point = Math.floor(Math.random() * Quotes.length);
  }
</script>

<main class="main-screen">
  <h1 class="text-center leading-10 text-2xl text-slate-800 sm:text-4xl title w-80 sm:w-3/4">
    <span class="text-5xl">"</span>
    {Quotes[point].quote}
    <span class="text-5xl">"</span>
  </h1>
  <h2 class=" text-lg bg-slate-800 rounded text-white p-1 mt-5 mb-10">
    {Quotes[point].coach}
  </h2>
  <button class="btn-green" on:click={randomQuote}>Random Quote</button>
</main>
<Footer />

<style>
  .title {
    animation: roling linear 10s infinite;
  }
  @keyframes roling {
    0% {
      transform: translate(0, 0);
    }
    50% {
      transform: translate(0, 10px);
    }
    100% {
      transform: translate(0, 0);
    }
  }
</style>
