<template>
  <div id="app">
    <main>
      <img alt="Vue logo" src="./assets/logo.png">
      <InfoBox
        type="warning"
        group="The heading's heading"
        heading="Yolo"
        body="Lorem ipsum doler sit amet"
      />
      <InfoBox
        type="info"
        group="Group"
        heading="This is an important message"
        body="Lorem ipsum doler sit amet"
      />
      <HelloWorld msg="This be an elegant message"/>
    </main>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import InfoBox from './components/InfoBox.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    InfoBox
  }
}
</script>

<style>
html, body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 60px 0 0 0;
  background-color: #8e98a3;
}
main {
  box-shadow: 0 0 10px 10px #2c3e5057;
  border-radius: 8px;
  max-width: 80%;
  margin: 0 auto;
  background-color: white;
}
</style>
