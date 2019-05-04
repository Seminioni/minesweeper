<template>
  <div
    :style="dimensions"
    class="minesweeper bd-left-color-white bd-top-color-white bordered"
  >
    <header class="minesweeper-header bd-bottom-color-white bd-right-color-white bordered">
      <counter
        class="bombs-left-counter"
        number="777"
      ></counter>
      <funny-ebalo></funny-ebalo>
      <counter
        class="time-left-counter"
        number="666"
      ></counter>
    </header>
    <main
      class="field"
      ref="field"
    >
      <div
        :key="i"
        class="field-cell"
        v-for="i in 200"
      >1</div>
    </main>
  </div>
</template>

<script>
  import Counter from "@/components/Counter";
  import FunnyEbalo from "@/components/FunnyEbalo";

  export default {
    props: {
      size: {
        default: 300
      }
    },

    components: {
      Counter,
      FunnyEbalo
    },

    computed: {
      dimensions() {
        return {
          width: `${this.size}px`,
          height: `${this.size}px`
        };
      }
    },

    mounted() {
      console.log(this.$refs.field.clientWidth);
    }
  };
</script>

<style lang="scss">
  .minesweeper {
    background-color: var(--c-bg-gray);
    min-height: 300px;
    padding: 8px;
  }

  .minesweeper-header {
    height: 40px;
    padding: 5px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
  }

  .field {
    display: flex;
    flex-wrap: wrap;
    height: calc(100% - 50px);
  }

  .field-cell {
    width: 15px;
    height: 15px;
  }
</style>
