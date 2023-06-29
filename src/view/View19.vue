<template>
  <div>
    <h2>
      {{userService.getLoginUser()}}
    </h2>
  </div>
</template>

<script setup lang="ts">

/**
 * 实体类
 */
interface User
{
  id: number;
  name: string;
}

/**
 * 接口
 */
interface UserService
{
  /**
   * 登录
   */
  login(user: User): void

  /**
   * 得到当前登录人的信息
   */
  getLoginUser(): User
}

/**
 * 实现类
 */
class UserServiceImpl implements UserService
{
  getLoginUser(): User
  {
    return {id: 100001, name: '张三'};
  }

  login(user: User): void
  {
    console.log(user)
  }
}

const userService: UserService = new UserServiceImpl();

const loginUser = userService.getLoginUser();
console.log(loginUser)
userService.login(loginUser);

console.log()

</script>

<style scoped>

</style>
