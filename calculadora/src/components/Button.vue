<template>
  <button class="button"
    @click="$emit('onClick', label)"
    :class="{ double, triple, operation }"
  >
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: {},
    operation: { type: Boolean },
    double: { type: Boolean },
    triple: { type: Boolean }
  }
}
</script>

<style lang="scss">
  .button {
    background-color: #f0f0f0;
    font-size: 1.4em;
    border: none;
    border-right: solid 1px #888;
    border-bottom: solid 1px #888;
    outline: none;

    &:active {
      background-color: #ccc;
    }

    &.double {
      grid-column: span 2;
    }

    &.triple {
      grid-column: span 3;
    }

    &.operation {
      background-color: #fa8231;
      color: #FFF;
    }

    &.operation:active {
      background-color: #fa8231cc;
    }
  }
</style>
