<template>
  <div>
    <h3>{{ user.name }}</h3>
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
};
</script>
