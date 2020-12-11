<template>
  <main class="box">
    <ComputedProperties :firstName="'Fabrício'" :lastName="'Pinto Ferreira'" />
    <Methods />
  </main>
  <footer>
    <p align="center" class="font-weight-bold">Fabreco</p>
    <!-- <Menu /> -->
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Menu from '../components/Menu.vue';
import ComputedProperties from '../components/ComputedProperties.vue';
import Methods from '../components/Methods.vue';

export default defineComponent({
  name: 'Computed',
  components: {
    // Menu,
    ComputedProperties,
    Methods,
  },
});
</script>

<style scoped>
.box {
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap;
  flex: 1 0 auto;
}
</style>
