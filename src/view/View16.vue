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
}

const user: User = new User();
//Cannot assign to 'id' because it is a read-only property.
user.id = 10002;
user.name = "张三";

console.log(user.id)
console.log(user.name)

</script>

<style scoped>

</style>
