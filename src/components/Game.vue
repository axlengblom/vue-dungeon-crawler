<template>
  <div v-for="monster in monsters" :key="monster.index">
    <h1>{{ monster.name }}</h1>
    <button @click="showUrl(monster.url)">More Info</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      monsters: [],
      currentMonster: [],
    };
  },
  methods: {
    showUrl(monsterUrl) {
      fetch('https://www.dnd5eapi.co' + monsterUrl)
        .then((res) => res.json())
        .then((data) => (this.currentMonster = data));
      console.log(this.currentMonster);
    },
  },
  mounted() {
    fetch('https://www.dnd5eapi.co/api/monsters')
      .then((response) => response.json())
      .then((data) => (this.monsters = data.results));
  },
};
</script>

<style></style>
