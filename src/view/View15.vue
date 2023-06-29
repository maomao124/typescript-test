<template>
  <div>
    <h2>{{ stu4 }}</h2>
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
  private id: number;
  /**
   * 姓名
   */
  protected name: string;
  /**
   * 性别
   */
  public sex: string;


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

const stu4: Student = new Student(102224, "王五", '女')

console.log(stu4)

//Property 'id' is private and only accessible within class 'Student'.
console.log(stu4.id)
//Property 'name' is protected and only accessible within class 'Student' and its subclasses.
console.log(stu4.name)
console.log(stu4.sex)

</script>

<style scoped>

</style>
