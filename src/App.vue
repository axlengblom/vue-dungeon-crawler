<template>
  <div id="app"></div>
  <div class="header"><h2>Dungeon Raider</h2></div>
  <Login />

  <Game :room="roomInfo.room[0].name">
    <p>{{ roomInfo.room[0].description }}</p>
    <h2>Monster</h2>
    <h3>{{ roomInfo.room[0].monster.monsterName }}</h3>
    <p>Weakness : {{ roomInfo.room[0].monster.monsterWeakness }}</p>
    <h2>Actions</h2>
    <p>This will be all the actions available in the room</p>
  </Game>
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
    return {
      roomInfo: {
        room: [
          {
            name: 'Room 1',
            description:
              'This room is filled with water, you are on a boat and see something slimy make its way up the bow',
            monster: {
              monsterName: 'Chutulu',
              monsterWeakness: 'Air',
            },
          },
          {
            name: 'Room 2',
            monster: {
              monsterName: 'Godzilla',
              monsterWeakness: 'None',
            },
          },
        ],
      },
    };
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
