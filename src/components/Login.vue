<template>
  <div>
    <input :value="user.name" placeholder="Choose a name" />
    <br />
    <button @click="create">Create Character</button>
  </div>
</template>

<script>
import { user } from '../app.js';

export default {
  name: 'Login',
  data() {
    return {
      user,
    };
  },
  methods: {
    create() {
      const userName = user.name;

      console.log(user.name);
      user.loggedIn = true;
      console.log(user.loggedIn);
    },
  },
};
</script>
