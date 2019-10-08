<template>
  <div :class="{
    [$style.root]: true,
    [$style.warning]: isWarning,
    [$style.didyouknow]: isDidyouknow,
    [$style.help]: isHelp,
    [$style.wide]: wide,
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
  name: 'InfoBox',
  props: {
    type: {
      type: String,
      required: true,
    },
    wide: Boolean,
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
    },
    isDidyouknow() {
      return this.type === 'didyouknow'
    },
    isHelp() {
      return this.type === 'help'
    }
  }
}
</script>

<style module>
  .root {
    padding: 20px 20px 8px 20px;
    border: none;
    border-left: 5px solid rgb(231, 213, 107);
    border-radius: 8px;
    background-color: #fefff1;
    margin: 20px 0;
    box-shadow: 0 0 3px 3px rgba(0, 0, 0, 0.05);
    width: 60%;
    float: right;
  }
  .wide {
    width: auto;
    float: none;
    clear: both;
  }
  .warning {
    border-left: 5px solid rgb(214, 104, 104);
    background-color: #fff1f1;
  }
  .didyouknow {
    border-left: 5px solid rgb(104, 148, 214);
    background-color: #f1f4ff;
  }
  .help {
    border-left: 5px solid rgb(104, 214, 190);
    background-color: #f1fffc;
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