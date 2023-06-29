<template>

</template>

<script lang="ts" setup>

function ref<T>(arg: T): T
{
  return arg;
}

console.log(ref("hello"))
console.log(ref(12345))
console.log(ref(true))
console.log(ref(null))
console.log(ref(undefined))

console.log(typeof ref("hello"))
console.log(typeof ref(12345))
console.log(typeof ref(true))
console.log(typeof ref(null))
console.log(typeof ref(undefined))

</script>

<style scoped>

</style>
