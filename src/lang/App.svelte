<script>
  import { t, locale, locales } from "./i18n";
	
	// Create a locale specific timestamp
  $: time = new Date().toLocaleDateString($locale, {
    weekday: "long",
    year: "numeric",
    month: "long",
    day: "numeric",
  });
</script>

<main>
  <div class="language-selector">
    <select class="locale-select" bind:value={$locale} >
      {#each locales as l (l)}
        <option value={l} key={l} o >
          {l === "ar" ? "عربي" : "English"}
        </option>
      {/each}
    </select>
  </div>
</main>

<style>
  main {
    display: flex;
    justify-content: center;
    align-items: center;
    width: fit-content;
    background-color: #f8f8f8;
    /* Add more styles if needed */
  }

  .language-selector, .locale-select {
    text-align: center;
    border: none;
  }

  .locale-select:focus, .language-selector:active {
    outline: none;
    border: none;
  }

  label {
    font-size: 16px;
    margin-right: 10px;
    border: none;
  }

  select {
    padding: 8px;
    font-size: 14px;
    cursor: pointer;
    width: fit-content;
    border: none;
  }
</style>
