<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  expose: ['ref2', 'ref4'],

  setup() {
    const ref1 = ref(1)
    const ref2 = ref(2)
    const ref3 = ref(3)
    const ref4 = ref(4)

    return { ref1, ref2 }
  },
})
</script>

<template>
  <div>
    child setup function (with options APIs' expose)
    <br>
    ref1: {{ ref1 }}
    <br>
    ref2: {{ ref2 }}
  </div>
</template>
