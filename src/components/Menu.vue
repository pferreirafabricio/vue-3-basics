<template>
  <section>
    <nav class="menu" @click="show('Fabreco')">
      <a href="#">
        <i class="fas fa-search"></i>
      </a>
      <a href="#">
        <i class="fas fa-plus-circle"></i>
      </a>
      <a href="#">
        <i class="fas fa-user-circle"></i>
      </a>
    </nav>
  </section>
</template>

<script lang="ts">
import { computed, defineComponent, ref } from 'vue';
import showName from '@/functions/show';

export default defineComponent({
  name: 'Menu',
  setup() {
    const count = ref<number>(0);
    const myName = computed(() => `My name is ${count.value}`);
    const show = showName;

    return {
      count,
      myName,
      show,
    };
  },
});

</script>

<style scoped>
.menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 20%;
  margin: 0 auto;
}

.menu a {
  color: var(--dark);
  font-size: var(--font-extra-large);
}

.menu a:hover {
  text-shadow: 0 4px 8px var(--dark-alpha);
}
</style>
