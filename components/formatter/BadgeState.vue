<script>

export default {
  props: {
    value: {
      type:     String,
      default: ''
    },
    row: {
      type:     Object,
      required: true
    },
    col: {
      type:     Object,
      default: () => {}
    },
  },
};
</script>

<template>
  <span :class="{'badge-state': true, [row.stateBackground]: true}">
    {{ row.stateDisplay }}
  </span>
</template>

<style lang="scss">
  @import "~assets/styles/base/_mixins.scss";

  .badge-state {
    padding: 5px 5px 5px 0;
    border: 1px solid transparent;
    border-radius: 2px;

    // Successful states are de-emphasized by using [text-]color instead of background-color
    &.bg-success {
      color: var(--success);
      background: transparent;
    }
  }

  .sortable-table TD .badge-state {
    @include clip;
    display: inline-block;
    max-width: 100%;
    position: relative;
    padding: 1px 10px 1px 0;
    font-size: 1em;
    max-width: 110px;
    font-size: .85em;
    vertical-align: middle;
  }
</style>
