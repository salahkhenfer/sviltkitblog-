<script>
  import { t, locale, locales } from './i18n'
 // Subscribe to locale changes and update local storage

locale.subscribe((value) => {
  // Update the locale store with the new value
  locale.update(() => value);
});
  // Create a locale specific timestamp
  $: time = new Date().toLocaleDateString($locale, {
    weekday: 'long',
    year: 'numeric',
    month: 'long',
    day: 'numeric',
  })
</script>

<main>
  <div class="language-selector">

    <select id="locale-select" bind:value={$locale}>
      {#each locales as l}
        <option value={l} key={l}>{l}</option>
      {/each}
    </select>
  </div>

</main>

<style>
  main {
    display: flex;
    justify-content: center;
    align-items: center;
    /* height: 100vh; */
    background-color: #f8f8f8;
    outline: none;
        border: none;

  }

  .language-selector {
    text-align: center;
    border: none;

  
  }
  .locale-select {
    text-align: center;
    border: none;

    width: 60px;
  }
  .language-selector:active {
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
 
    border-radius: 4px;
    cursor: pointer;
        width: 60px;
            border: none;
            

  }

</style>