<template>
  <div id="app"></div>
  <div class="header"><h2>Dungeon Raider</h2></div>
  <Login />

  <Game @onshowUrl="showUrl(monster)"> </Game>
</template>

<script>
import Game from './components/Game.vue';
import Login from './components/Login.vue';

export default {
  name: 'App',

  components: {
    Login,
    Game,
  },

  data() {
    return {};
  },
  methods: {
    showUrl() {
      console.log('fisk');
    },
  },
};
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

.todos ul {
  display: flex;
  flex-direction: column;
}
</style>
