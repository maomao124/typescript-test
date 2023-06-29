<template>
  <div>
    <h2>{{ user }}</h2>
  </div>
</template>

<script lang="ts" setup>

import {onBeforeMount, onMounted} from "vue";

interface User
{
  id: number,
  name: string,
  age: number,

  getName(): string

  getAgeString(): string

  setName(name: string): void
}

const user: User = {
  id: 10002,
  name: "张三",
  age: 12,
  getName(): string
  {
    return this.name
  },
  getAgeString(): string
  {
    if (this.age < 0 || this.age > 120)
    {
      return "年龄输入错误"
    }
    if (this.age < 18)
    {
      return "未成年";
    }
    if (this.age < 30)
    {
      return "青年"
    }
    if (this.age < 60)
    {
      return "中年"
    }
    return "老年"
  },
  setName(name: string)
  {
    this.name = name;
  }
}

onBeforeMount(()=>
{
  console.log(user.getName())
  console.log(user.getAgeString())
  user.setName("李四")
  console.log(user.getName())
})

</script>

<style scoped>

</style>
