<script lang="ts">
export default {
  expose: ['ref2', 'ref4'],

  data() {
    return {
      ref1: 1,
      ref2: 2,
      ref3: 3,
      ref4: 4,
    }
  }
}
</script>

<template>
  <div>
    child options APIs
    <br>
    ref1: {{ ref1 }}
    <br>
    ref2: {{ ref2 }}
  </div>
</template>
