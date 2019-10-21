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
:root {
  --mog-turqoise: rgb(140, 206, 198); /* True FF9 Mog-turqouise */
  --warning-red: rgb(214, 104, 104);
  --attention-yellow: rgb(224, 203, 83);
  --funfact-blue: rgb(104, 148, 214);
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
    /*opacity: 0.65;*/
    font-size: 0.7rem;
    letter-spacing: 1px;
    margin-bottom: 3px;
  }
  hr {
    height: 0;
    border: none;
    border-top: 3px solid rgba(68, 68, 68, 0.2);
    margin: 0.95em 0;
    opacity: .45;
  }
  ul, ol {
    margin-left: 0;
    padding-left: 20px;
    list-style-type: initial;
  }
  li {
    display: list-item;
    line-height: 140%;
  }
  a {
    color: white;
    text-decoration: none;
    padding: 2px 3px;
    border-radius: 2px;
    border: 2px solid transparent;
    transition: border 300ms linear;
  }
    a:hover, a:active, a:focus {
      border-color: rgba(0,0,0,0.4);
    }

  .wide {
    width: auto;
    float: none;
    clear: both;
  }
  .warning {
    border-left: 5px solid var(--warning-red);
    background-color: rgba(214, 104, 104, 0.3);
  }
    .warning a {
      background-color: var(--warning-red);
    }
    .warning hr {
      border-color: var(--warning-red);
    }
    .warning h6 {
      color: var(--warning-red);
    }
  .didyouknow {
    border-left: 5px solid var(--funfact-blue);
    background-color: rgba(104, 148, 214, 0.2);
  }
    .didyouknow a {
      background-color: var(--funfact-blue);
    }
    .didyouknow hr {
      border-color: var(--funfact-blue);
    }
    .didyouknow h6 {
      color: var(--funfact-blue);
    }
  .dontmiss {
    border-left: 5px solid var(--attention-yellow);
    background-color: #fefff1;
  }
    .dontmiss a {
      background-color: var(--attention-yellow);
    }
    .dontmiss hr {
      border-color: var(--attention-yellow);
    }
    .dontmiss h6 {
      color: var(--attention-yellow);
    }
  .help {
    border-left: 5px solid var(--mog-turqoise);
    background-color: rgba(140, 206, 198, 0.30);
  }
    .help a {
      background-color: var(--mog-turqoise);
    }
    .help hr {
      border-color: var(--mog-turqoise);
    }
    .help h6 {
      color: var(--mog-turqoise);
    }
</style>