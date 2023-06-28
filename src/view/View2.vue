<template>
  <div>
    <h1>{{ user }}</h1>
  </div>
</template>

<script setup lang="ts">
interface User
{
  id: number
  name: string,
  age: number,
}

function printUser(user: User)
{
  console.log("user.id=" + user.id)
  console.log("user.name=" + user.name)
  console.log("user.age=" + user.age)
}

const user: User = {
  id: 10001,
  name: '张三',
  age: 19
}

printUser(user);

</script>

<style scoped>

</style>
