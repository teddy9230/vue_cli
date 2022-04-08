<template>
  <div class="Hook">
    <h1>{{ title }}</h1>
    <button @click="ChangeTitle">點我</button>
  </div>
</template>

<script>
export default {
  name: "Hook",
  data() {
    return { title: "請點我" };
  },
  methods: {
    ChangeTitle() {
      this.title = "點我完成";
    },
  },
  beforeCreate() {
    alert("Before Acreated Hook");
  },
  created() {
    alert("Created Hook");
  },
  beforeUpdate() {
    alert("Before Update Hook");
  },
};
</script>

<style>
</style>