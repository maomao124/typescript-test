<template>
  <div>
    <h1>{{ str }}</h1>
  </div>
</template>

<script setup lang="ts">

const str: string = 'hello world';

function hello(str: string): void
{
  console.log(str);
}

hello(str);


</script>

<style scoped>

</style>
