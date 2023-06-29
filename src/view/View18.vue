<template>

</template>

<script setup lang="ts">

class Student
{
  private _id: number;
  private _name: string;

  get name(): string
  {
    console.log("调用name 的get方法")
    return this._name;
  }

  set name(value: string)
  {
    console.log("调用name 的set方法")
    this._name = value;
  }

  get id(): number
  {
    console.log("调用id 的get方法")

    return this._id;
  }

  set id(value: number)
  {
    console.log("调用id 的set方法")
    this._id = value;
  }

  constructor()
  {
    this._id = 10001
    this._name = "";
  }
}

const student: Student = new Student();

//Property '_id' is private and only accessible within class 'Student'.
//console.log(student._id)
//Property '_name' is private and only accessible within class 'Student'.
//console.log(student._name)

student.id = 99999;
student.name = "李四"

console.log(student.id)
console.log(student.name)

</script>

<style scoped>

</style>
