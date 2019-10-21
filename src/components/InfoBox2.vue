<template>
  <div class="infobox2" :class="{
    [$style.warning]: isWarning,
    [$style.didyouknow]: isDidyouknow,
    [$style.dontmiss]: isDontMiss,
    [$style.help]: isHelp,
    [$style.wide]: wide,
  }">
    <h6>{{ group }}</h6>
    <h3>{{ heading }}</h3>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'InfoBox2',
  props: {
    type: String,
    wide: Boolean,
    group: {
      type: String,
      default: "Some topic",
    },
    heading: String
  },
  computed: {
    isWarning() {
      return this.type === 'warning'
    },
    isDidyouknow() {
      return this.type === 'didyouknow'
    },
    isDontMiss() {
      return this.type === 'dontmiss'
    },
    isHelp() {
      return this.type === 'help'
    }
  }
}
</script>

<style>
  .infobox2 {
    padding: 20px 20px 20px 20px;
    border: none;
    border-radius: 8px;
    margin: 20px 0;
    box-shadow: 0 0 3px 3px rgba(0, 0, 0, 0.05);
    width: 60%;
    float: right;
  }
</style>
<style module>
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
  .dontmiss {
    border-left: 5px solid rgb(231, 213, 107);
    background-color: #fefff1;
  }
  .help {
    border-left: 5px solid rgb(140, 206, 198);
    background-color: rgba(140, 206, 198, 0.30);
  }
  p, h3, h6 {
    margin: 0;
    padding: 0;
  }
  p {
    margin-top: 12px;
    line-height: 140%;
  }
  p:first-child {
    margin-top: 0;
  }
  h6 {
    text-transform: uppercase;
    font-weight: bold;
    opacity: 0.65;
    font-size: 0.7rem;
    letter-spacing: 1px;
    margin-bottom: 3px;
  }
  hr {
    height: 0;
    border: none;
    border-top: 3px solid rgba(68, 68, 68, 0.2);
    margin: 0.95em 0;
  }
  ul, ol {
    margin-left: 0;
    padding-left: 20px;
  }
  li {
    display: list-item;
  }
</style>