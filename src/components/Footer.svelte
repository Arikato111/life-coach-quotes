<script>
  import GithubIcon from "./icons/GithubIcon.svelte";
</script>

<footer>
  <div
    class="fixed left-0 bottom-0 m-2 py-1 px-2 rounded bg-yellow-200 dark:bg-yellow-600 dark:text-slate-200"
  >
    <a href="/quotes.json"> view quotes.json </a>
  </div>
  <a
    target="_blank"
    title="view source code"
    rel="noreferrer"
    href="https://github.com/Arikato111/life-coach-quotes"
  >
    <div
      class="fixed fill-black dark:fill-white right-0 bottom-0 inline-block m-2 w-14"
    >
      <GithubIcon />
    </div>
  </a>
</footer>
