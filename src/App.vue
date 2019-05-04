<template lang="html">
    <div id="app">
      <mine-sweeper size='400'></mine-sweeper>
    </div>
</template>

<script>
  import "normalize.css";
  import MineSweeper from "@/components/MineSweeper";

  export default {
    name: "app",
    components: {
      MineSweeper
    }
  };
</script>

<style lang="scss">
  *:before,
  *:after,
  * {
    box-sizing: border-box;
  }

  html,
  body {
    box-sizing: inherit;
    height: 100%;
  }

  body {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
