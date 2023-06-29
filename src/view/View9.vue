<template>
  <div>

  </div>
</template>

<script lang="ts" setup>

/**
 * 打印字符串到控制台
 * @param str 字符串
 * @param alignment 对齐方式，只能取值left、right和center
 */
function print(str: string, alignment: "left" | "right" | "center")
{
  console.log(str, alignment)
}

print("hello", "left")
print("hello", "right")
print("hello", "center")
//以下报错：Argument of type '"131412351"' is not assignable to parameter of type '"left" | "right" | "center"'
//print("hello","131412351")


</script>

<style scoped>

</style>
