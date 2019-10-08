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
/**
 * TODO: 
 * Toggle sink wrapper on or off?
 */
export default {
  name: 'SinkBox',
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
      inset 0px 10px 10px -10px rgba(0, 0, 0, 0.308),
      inset 0px -10px 10px -10px rgba(0, 0, 0, 0.308);
    min-height: 100px;
    background-color: #ced3d8b9;
    margin: 20px -20px;
    padding: 20px 20px 8px 20px;
  }
  header p, header h3 {
    margin: 0;
  }
  header small {
    text-transform: uppercase;
    font-weight: bold;
    opacity: 0.65;
    font-size: 0.7rem;
    letter-spacing: 1px;
  }
</style>