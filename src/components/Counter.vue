<template>
  <div class="counter">
    <i class="digit" :class="first"></i>
    <i class="digit" :class="second"></i>
    <i class="digit" :class="third"></i>
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
      first() {
        const digit = this.getNumberDigitAt(0);
        return this.getClassNameByDigit(digit);
      },
      second() {
        const digit = this.getNumberDigitAt(1);
        return this.getClassNameByDigit(digit);
      },
      third() {
        const digit = this.getNumberDigitAt(2);
        return this.getClassNameByDigit(digit);
      }
    },

    methods: {
      getNumberDigitAt(position) {
        return this.number.charAt(position);
      },
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
