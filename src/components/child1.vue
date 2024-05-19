<script setup lang="ts">
import { ref } from 'vue';

const ref1 = ref(1)
const ref2 = ref(2)
const ref3 = ref(3)
const ref4 = ref(4)

defineExpose({ ref2, ref4 })
</script>

<template>
  <div>
    child script setup
    <br>
    ref1: {{ ref1 }}
    <br>
    ref2: {{ ref2 }}
  </div>
</template>
