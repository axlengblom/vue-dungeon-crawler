<template>
  <div v-for="monster in monsters" :key="monster.index">
    <h1>{{ monster.name }}</h1>
    <button @click="$emit('onshowUrl', monster)">More Info</button>
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
  methods: {},
  mounted() {
    fetch('https://www.dnd5eapi.co/api/monsters')
      .then((response) => response.json())
      .then((data) => (this.monsters = data.results));
  },
};
</script>

<style></style>
