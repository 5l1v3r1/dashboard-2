<script>
export default {};
</script>

<template>
  <div class="info-box">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
  .info-box {
    background-color: var(--tabbed-container-bg);
    border: 1px solid var(--tabbed-border);
    padding: 20px;
    border-radius: var(--border-radius);
    .info-column:not(:last-child) {
      border-right: 1px solid var(--tabbed-border);
    }
    .info-row {
      margin-bottom: 10px;
      .info-row-label {
        padding-top: 2px;
        display: inline-block;
      }
    }
    .info-column,
    .info-row {
      label {
        color: var(--input-label);
      }
    }

    .info-column {
      .usage {
        margin-bottom: 10px;
        label {
          display: inline-block;
          font-size: 12px;
          padding-top: 6px;
        }
      }
      .flex-item-half {
        align-items: center;
      }
    }
  }
</style>
