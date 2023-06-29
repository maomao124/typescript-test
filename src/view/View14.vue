<template>
  <div>
    <h2>{{stu1}}</h2>
    <h2>{{stu2}}</h2>
    <h2>{{stu3}}</h2>
    <h2>{{stu4}}</h2>


  </div>
</template>

<script setup lang="ts">

/**
 * 学生类
 */
class Student
{
  /**
   * id
   */
  id: number;
  /**
   * 姓名
   */
  name: string;
  /**
   * 性别
   */
  sex: string;


  /**
   * 无参构造方法
   */
  constructor();
  /**
   *
   * @param id 学生学号
   */
  constructor(id: number);
  /**
   *
   * @param id 学生学号
   * @param name 姓名
   */
  constructor(id: number, name: string);
  /**
   *
   * @param id 学生学号
   * @param name 姓名
   * @param sex 性别
   */
  constructor(id: number, name: string, sex: string);
  /**
   *
   * @param id 学生学号
   * @param name 姓名
   * @param sex 性别
   */
  constructor(id?: number, name?: string, sex?: string)
  {
    console.log("构造方法被调用了")
    this.id = id ? id : 10001
    this.name = name ? name : "张三"
    this.sex = sex ? sex : "男"
  }
}

const stu1: Student = new Student()
console.log(stu1)

const stu2: Student = new Student(102222)
console.log(stu2)

const stu3: Student = new Student(102223, "李四")
console.log(stu3)

const stu4: Student = new Student(102224, "王五", '女')
console.log(stu4)

console.log(stu4.name)

</script>

<style scoped>

</style>
