<template>
  <div>
  </div>
</template>

<script setup lang="ts">

class C1
{
  study()
  {
    console.log("C1 study")
  }
}

class C2 extends C1
{
  study()
  {
    super.study();
    console.log("C2 study")
  }
}

let c: C1 = new C2()
c.study();

c = new C1()
c.study();


</script>

<style scoped>

</style>
