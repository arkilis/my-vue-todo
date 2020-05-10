<template>
    <span>
      <input :myValue="myValue" v-bind:value="myValue" />
      <button>Edit</button>
      <button>Delete</button>
    </span>    
</template>

<script>
  // 组件逻辑
  // 在.vue文件中，需要默认export一个Vue实例
  export default {
    name: "MyTodoView",
    props: {
      myValue: {
        type: String,
        default: ""
      }
    }
  };
</script>

<style>
  /* 组件样式 */
</style>