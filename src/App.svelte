<script lang="ts">
  import "./App.css";
  import { onMount } from "svelte";
  import Footer from "./components/Footer.svelte";
  import Quotes from "../public/quotes.json";
  import TheQuote from "./components/TheQuote.svelte";
  import ToggleMode from "./components/ToggleMode.svelte";
  import { checkTheme } from "./components/CheckMode";
  checkTheme();

  let point: number = Math.floor(Math.random() * Quotes.length);

  onMount(() => {
    randomQuote();
  });

  function randomQuote() {
    point = Math.floor(Math.random() * Quotes.length);
  }
</script>

<main class="main-screen">
  <ToggleMode />
  <div class="text-lg dark:text-slate-200">Life coach quotes</div>
  <TheQuote quote={Quotes[point].quote} coach={Quotes[point].coach} />
  <button class="btn-green" title="click to random quote" on:click={randomQuote}
    >Random Quote</button
  >
</main>
<Footer />
