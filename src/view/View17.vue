<template>

</template>

<script lang="ts" setup>

class User
{
  /**
   * 用户编号，只读
   */
  readonly id: number;
  /**
   * 用户名称
   */
  name: string | undefined;

  constructor()
  {
    this.id = 10001;
  }

  /**
   * 转字符串
   */
  toString()
  {
    return "用户编号：" + this.id + ",用户名称：" + this.name
  }

  /**
   * 转json
   */
  toJson()
  {
    return JSON.stringify(this);
  }

}

const user: User = new User();
user.name = "张三";

console.log(user.id)
console.log(user.name)

console.log(user.toString())
console.log(user.toJson())

</script>

<style scoped>

</style>
