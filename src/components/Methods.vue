<template>
  <article>
    <h2>Methods</h2>
    <div>
      <button @click="toggleTextDisplay">Click me</button>
      <transition name="fade">
        <span v-if="show" class="d-block">
          {{ clickedText }} &#x1F423;
        </span>
      </transition>
    </div>
  </article>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'ComputedProperties',
  setup() {
    const clickedText = ref<string>('Clicked!');
    const show = ref<boolean>(false);

    const toggleTextDisplay = () => {
      show.value = !show.value;
    };

    return {
      clickedText,
      show,
      toggleTextDisplay,
    };
  },
});
</script>
