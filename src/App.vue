<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Message from HelloWorld"/> -->
  <Homework v-if="isSentence" :msgc="message4" />
  <b><Homework :msg="message" :msgg="message2" :msggg="message3" /></b>
  <p><b>Wonders of the world list:</b></p>
  <ul>
    <ol v-for="(wonder, idx) in wonders" :key="idx"><b>  {{ wonder }} </b>
      <br> In lower case = {{ lowerCase(wonder) }} <br><br>
    </ol>
  </ul>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import Homework from './components/Homework.vue';

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Homework
  },
  data() {
    return {
      message: "The 7 wonders of the wodern world",
      message2: "Welcome",
      message3: "Visit website",
      message4: "Conditional message",
      isSentence: true,
      wonders: ["CHICHEN ITZA", "CHRIST THE REDEEMER", "TAJ MAHAL", "GREAT WALL OF CHINA", "MACHU PICCHU", "PETRA", "COLOSSEUM"],
    };
  },
  methods: {
    lowerCase(value) {
      return value.toLowerCase();
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background-color: #6f966f;
}

h1 {
  color: black;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

ul {
  color: white;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

p {
  color: black;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

img {
  box-shadow: 1px 1px 2px 2px #086308;
  width: 500px;
  border-radius: 20%;
}

img:hover{
  border-radius: 30%;
  cursor: pointer;
  width: 600px;
}

div {
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  font-size: xx-large;
  color: rgba(0, 0, 0, 0.899);
}

button {
  background-color: #086308;
  width: 200px;
  height: 50px;
  font-size: x-large;
  color: white;
  border: white;
  border-radius: 50%;
  font-weight: 300;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

button:hover {
  background-color: #48db48;
  width: 180px;
  height: 50px;
  font-size: x-large;
  color: black;
  border: white;
  border-radius: 50%;
  cursor: pointer;
}</style>
