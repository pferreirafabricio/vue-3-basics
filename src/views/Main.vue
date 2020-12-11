<template>
  <main>
    <ComputedProperties :firstName="'Fabrício'" :lastName="'Pinto Ferreira'" />

    <footer>
      <Menu />
    </footer>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Menu from '../components/Menu.vue';
import ComputedProperties from '../components/ComputedProperties.vue';

export default defineComponent({
  name: 'Computed',
  components: {
    Menu,
    ComputedProperties,
  },
});
</script>
