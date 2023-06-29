<template>

</template>

<script lang="ts" setup>

interface StudentV1
{
  id: number,
  name: string,
  sex: string,
  age: number
}

interface StudentV2
{
  id: number,
  name: string,
  sex?: string,
  age?: number
}

//Property 'age' is missing in type '{ id: number; name: string; sex: string; }' but required in type 'StudentV1'.
const studentV1: StudentV1 = {id: 10001, name: "张三", sex: "男"};
//Type 'undefined' is not assignable to type 'number'.
const student2V1: StudentV1 = {id: 10001, name: "张三", sex: "男", age: undefined};
//并不会报错
const studentV2: StudentV2 = {id: 10001, name: "张三"};
const student2V2: StudentV2 = {id: 10001, name: "张三",sex:undefined};

console.log(studentV1)
console.log(studentV2)
console.log(student2V1)
console.log(student2V2)

</script>

<style scoped>

</style>
