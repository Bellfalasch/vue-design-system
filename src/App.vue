<template>
  <div id="app">
    <main>
      <!--<img alt="Vue logo" src="./assets/logo.png">-->
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptas illo minus dolor molestias sapiente natus omnis animi, eum, odit ea excepturi debitis quae explicabo quos quibusdam tempore eos totam rem?
      <InfoBox2
        type="dontmiss"
        group="Don't miss!"
        heading="Rare item #2"
      >
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ad voluptatibus hic recusandae in repellat ratione exercitationem laborum cum esse aut molestias amet, <a href="#">molestiae placeat</a>, voluptatum et aliquid error inventore impedit?</p>
      </InfoBox2>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem alias atque saepe necessitatibus quae rerum eos sunt enim, voluptatum provident illo earum quasi, possimus nisi, omnis quas suscipit ut doloribus.
      <InfoBox2
        type="warning"
        wide="true"
        group="The heading's heading"
        heading="Yolo"
      >
        <p>A most <a href="#">critical thing</a> will happen that cannot be undone, please proceed with caution.</p>
      </InfoBox2>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem alias atque saepe necessitatibus quae rerum eos sunt enim, voluptatum provident illo earum quasi, possimus nisi, omnis quas suscipit ut doloribus.
      <InfoBox2
        :wide="!true"
        group="Group"
        heading="This is an important message"
      >
        <p>This message is type-less, so it will render without colors. Lorem ipsum doler sit amet</p>
        <hr />
        <p>Divide <a href="#">a message</a> into sections.</p>
      </InfoBox2>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem alias atque saepe necessitatibus quae rerum eos sunt enim, voluptatum provident illo earum quasi, possimus nisi, omnis quas suscipit ut doloribus.
      <InfoBox2
        type="help"
        :wide="!true"
        group="Helpful advice"
        heading="Stuck?"
      >
        <p>Lorem ipsum doler sit amet, Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt repudiandae rerum commodi nam beatae, dicta sequi. Saepe voluptate eligendi tempora quia minus? Id quaerat ipsa placeat labore quis nam voluptate!</p>
        <ol>
          <li>We can <a href="#">add any HTML</a></li>
          <li>Into this</li>
        </ol>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eveniet praesentium voluptatibus tempore laboriosam fuga nisi aliquid nostrum, esse vitae. Eos incidunt dolores veniam explicabo at harum consequatur, a dolore vitae.</p>
      </InfoBox2>
      <InfoBox2
        type="didyouknow"
        wide="true"
        group="Did you know?"
        heading="Funny ..."
      >
        <p>Lorem <a href="#">ipsum doler sit</a> amet</p>
        <hr />
        <p>Divide a message into sections.</p>
      </InfoBox2>
      <SinkBox
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
import InfoBox2 from './components/InfoBox2.vue'
import SinkBox from './components/SinkBox.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    InfoBox,
    InfoBox2,
    SinkBox,
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
  padding: 20px;
}
p, h1, h2, h3, h4, li {
  max-width: 80%;
}
</style>
