<template>
  <div class="counter">
    <i class="digit" :class="digit.first"></i>
    <i class="digit" :class="digit.second"></i>
    <i class="digit" :class="digit.third"></i>
  </div>
</template>

<script>
  export default {
    props: {
      number: {
        default: "020"
      }
    },

    computed: {
      digit() {
        const numbers = this.number.split('');

        return {
          first: this.getClassNameByDigit(numbers[0]),
          second: this.getClassNameByDigit(numbers[1]),
          third: this.getClassNameByDigit(numbers[2])
        }
      },
    },

    methods: {
      getClassNameByDigit(digit) {
        return `digit-${digit}`;
      }
    }
  };
</script>

<style lang="scss">
  .counter {
    display: flex;
    width: 43px;
    height: 100%;
  }

  .digit {
    flex-grow: 1;
    flex-basis: 0;
    background: url("~@/assets/images/sprite.gif");
  }

  $px: 0;

  @for $i from 0 through 9 {
    .digit-#{$i} {
      background-position: #{$px}px 0;
    }

    $px: $px - 13;
  }
</style>
