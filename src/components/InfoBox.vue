<template>
  <div :class="{
    [$style.root]: true,
    [$style.warning]: isWarning
  }">
    <header>
      <p><small>{{ group }}</small></p>
      <h3>{{ heading }}</h3>
    </header>
    <p>{{ body }}</p>
  </div>
</template>

<script>
export default {
  name: 'InfoBox',
  props: {
    type: {
      type: String,
      required: true,
    },
    group: {
      type: String,
      default: "Some topic",
    },
    heading: String,
    body: String,
  },
  computed: {
    isWarning() {
      return this.type === 'warning'
    }
  }
}
</script>

<style module>
  .root {
    box-shadow:
      inset 0px 11px 8px -10px #000,
      inset 0px -11px 8px -10px #000;
    min-height: 100px;
    background-color: #ced3d8;
  }
  .warning {
    border: 1px solid red;
  }
</style>