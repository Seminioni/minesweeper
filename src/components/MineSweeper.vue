<template>
  <div class="minesweeper bd-left-color-white bd-top-color-white bordered">
    <header class="minesweeper-header bd-bottom-color-white bd-right-color-white bordered">
      <div class="bombs-left-to-find"></div>
      <div class="funny-face"></div>
      <div class="time-counter"></div>
    </header>
    <main class="field">
      <div class="field-row">
        <div class="field-cell"></div>
        <div class="field-cell"></div>
        <div class="field-cell"></div>
        <div class="field-cell"></div>
        <div class="field-cell"></div>
      </div>
    </main>
  </div>
</template>

<script>
  export default {};
</script>

<style lang="scss" scoped>
  .minesweeper {
    background-color: var(--c-bg-gray);
    min-height: 300px;
    width: 50vw;
    padding: 8px;
  }

  .minesweeper-header {
    min-height: 50px;
  }
</style>
