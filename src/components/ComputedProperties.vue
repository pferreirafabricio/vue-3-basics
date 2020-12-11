<template>
  <article>
    <h2>Computed Properties and props</h2>
    <span>
      {{ myName }}
    </span>
  </article>
</template>

<script lang="ts">
import { computed, defineComponent } from 'vue';

export default defineComponent({
  name: 'ComputedProperties',
  props: {
    firstName: String,
    lastName: String,
  },
  setup(props) {
    const myName = computed((): string => `${props.firstName} ${props.lastName}`);

    return {
      myName,
    };
  },
});
</script>
