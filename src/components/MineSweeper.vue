<template>
  <div class="minesweeper bd-left-color-white bd-top-color-white bordered">
    <header class="minesweeper-header bd-bottom-color-white bd-right-color-white bordered">
      <counter 
        class="bombs-left-counter"
        number="777">
      </counter>
      <funny-ebalo></funny-ebalo>
      <counter 
        class="time-left-counter"
        number="666">
      </counter>
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
  import Counter from "@/components/Counter";
  import FunnyEbalo from "@/components/FunnyEbalo";

  export default {
    components: {
      Counter,
      FunnyEbalo
    }
  };
</script>

<style lang="scss">
  .minesweeper {
    background-color: var(--c-bg-gray);
    min-height: 300px;
    width: 50vw;
    padding: 8px;
  }

  .minesweeper-header {
    height: 40px;
    padding: 5px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>
