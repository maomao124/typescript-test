<template>

</template>

<script lang="ts" setup>

interface Student
{
  id: number,
  name: string,
  sex: string,
  age: number
}

const student1: Student = {id: 10001, name: "张三", sex: "男", age: 19};

//报错，多了address
//const student3: Student = {id: 10001, name: "张三", sex: "男", age: 19, address: "中国"};

const student3 = {id: 10001, name: "张三", sex: "男", age: 19, address: "中国"};
//鸭子类型，student3并没有声明类型为Student，但它与 Student 类型有一样的属性，也可以被当作是 Student 类型

console.log(student1);
console.log(student3);

</script>

<style scoped>

</style>
