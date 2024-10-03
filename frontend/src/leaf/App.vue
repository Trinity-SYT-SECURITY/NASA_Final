<template>
  <WithStreamlitConnection v-slot="{ args }">
    <MyComponent :data="args.data" />
  </WithStreamlitConnection>
</template>

<script setup lang="ts">
import MyComponent from "./MyComponent.vue";
import WithStreamlitConnection from "../streamlit/WithStreamlitConnection.vue";
</script>

<style>
body,
html {
  height: 100%;
  margin: 0;
}
</style>
