<template>
  <Main />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Main from './views/Main.vue';

export default defineComponent({
  components: { Main },
  name: 'App',
});
</script>

<style>
@import './styles/main.css';
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;700&display=swap');

#app {
  font-family: 'Ubuntu', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
