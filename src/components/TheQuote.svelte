<script lang="ts">
  export let quote: string = "";
  export let coach: string = "";
</script>

<h1
  class="text-center leading-10 text-2xl text-slate-800 dark:text-slate-200 sm:text-4xl title w-80 sm:w-3/4"
>
  <span class="text-5xl">"</span>
  {quote}
  <span class="text-5xl">"</span>
</h1>
<h2 class="coach text-lg bg-slate-800 rounded text-white  p-1 mt-5 mb-10">
  {coach}
</h2>

<style>

  .coach{
    animation: scaling linear 10s infinite
  }
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

  @keyframes scaling {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.4);
    }
    100% {
      transform: scale(1);
    }
  }
</style>
