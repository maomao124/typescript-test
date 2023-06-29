<template>

</template>

<script lang="ts" setup>

function toUpperCase(str?: string | null): string
{
  return str?.toUpperCase() || "无效字符串"
}

function toUpperCase2(str: string): string
{
  return str.toUpperCase()
}

console.log(toUpperCase("hello"))
console.log(toUpperCase(null))
console.log(toUpperCase())

console.log(toUpperCase2("hello2"))
//Argument of type 'null' is not assignable to parameter of type 'string'.
//console.log(toUpperCase2(null))
//Expected 1 arguments, but got 0.
//console.log(toUpperCase2())

</script>

<style scoped>

</style>
