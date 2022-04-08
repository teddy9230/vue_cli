<template>
  <div id="onlinefriends">
    <h1>Online Friends</h1>
    <div v-for="(friend, index) in friends" :key="index">
      <h6 v-if="friend.online">{{ friend.name }}</h6>
    </div>
  </div>
</template>

<script>
export default {
  name: "OnlineFriends",
  props: ["friends"],
  data() {
    return {
      // friends: [
      //   { name: "A", online: true },
      //   { name: "B", online: false },
      //   { name: "C", online: true },
      //   { name: "D", online: false },
      //   { name: "E", online: false },
      // ],
    };
  },
};
</script>

<style>
#h6 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>