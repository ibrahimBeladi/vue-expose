<script setup lang="ts">
import { ref, onMounted, type Ref } from 'vue';
import child from './child1.vue';

const childRef = ref<InstanceType<typeof child> | null>(null)

onMounted(() => {
  // TS check, listing all refs
  // it should be only ref2 (and maybe ref4)

  console.log("\nparent script setup")
  // ref1 and ref2 are returned, ref2 is only exposed
  console.log(`ref1 = ${childRef?.value?.ref1}`)
  console.log(`ref2 = ${childRef?.value?.ref2}`)
  // ref3 and ref4 are NOT returned, ref4 is only exposed
  console.log(`ref3 = ${childRef?.value?.ref3}`)
  console.log(`ref4 = ${childRef?.value?.ref4}`)
})
</script>

<template>
  <child ref="childRef" />
</template>
