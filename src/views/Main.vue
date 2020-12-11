<template>
  <main class="box">
    <ComputedProperties :firstName="'Fabrício'" :lastName="'Pinto Ferreira'" />
    <Methods />
  </main>
  <footer>
    <p class="my-name font-weight-bold">Fabreco  &#x1F423;</p>
    <!-- <Menu /> -->
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ComputedProperties from '../components/ComputedProperties.vue';
import Methods from '../components/Methods.vue';

export default defineComponent({
  name: 'Main',
  components: {
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

.my-name {
  color: var(--dark-green);
  font-size: var(--font-extra-large);
}
</style>
