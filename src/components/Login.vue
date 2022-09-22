<template>
  <div><h3></h3></div>
</template>

<script>
import { reactive } from 'vue';

export const user = reactive({ name: '', loggedIn: 'false' });
export default {
  name: 'Login',
};
</script>
