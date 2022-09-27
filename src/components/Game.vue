<template>
  <h1>Welcome to {{ room }}</h1>
  <slot></slot>
</template>

<script>
export default {
  props: { room: String },
};
</script>

<style></style>
