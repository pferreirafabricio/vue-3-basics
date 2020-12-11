<template>
  <article>
    <h2>Methods and data</h2>
    <div>
      <button class="button font-weight-bold" @click="toggleTextDisplay">Click me</button>
      <transition name="fade">
        <span v-if="show">
          &nbsp; {{ clickedText }} &#x1F423;
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

<style scoped>
.button {
  background: var(--green-gradient);
  border: none;
  width: 120px;
  height: 24px;
  box-shadow: 0 4px 10px var(--green-alpha);
}
</style>
