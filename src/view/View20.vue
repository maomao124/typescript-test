<template>
  <div>
  </div>
</template>

<script setup lang="ts">

interface Flyable
{
  fly(): void
}

class Animal
{
  name: string;

  constructor(name: string)
  {
    this.name = name
  }
}

class Bird extends Animal implements Flyable
{
  fly()
  {
    console.log(`${this.name}在飞翔`)
  }
}

const b: Flyable & Animal = new Bird("小黄鸟")
b.fly()

</script>

<style scoped>

</style>
