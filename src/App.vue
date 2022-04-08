<template>
  <div id="app">
    <h2>{{ title }}</h2>
    <!-- <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Post</a></li>
        <li><a href="">About</a></li>
      </ul>
    </nav> -->
    <!-- <Navbar></Navbar> -->
    <!-- <Hook></Hook> -->
    <Post></Post>
    <!-- <AllFriends :friends="friends" @delete="deleteFriend"></AllFriends> -->
    <!-- <OnlineFriends :friends="friends"></OnlineFriends> -->
  </div>
</template>

<script>
// import Navbar from "./components/Navbar.vue";
// import Hook from "./components/Hook.vue";
import Post from "./components/Axios.vue";
// import AllFriends from "./components/props/AllFriends.vue";
// import OnlineFriends from "./components/props/OnlineFriends.vue";

export default {
  name: "App",
  data() {
    return {
      title: "App.vue",
      friends: [
        { name: "A", online: true },
        { name: "B", online: false },
        { name: "C", online: true },
        { name: "D", online: false },
        { name: "E", online: false },
      ],
    };
  },
  components: {
    // Navbar,
    // Hook,
    Post,
    // AllFriends,
    // OnlineFriends,
  },
  methods: {
    deleteFriend(payload) {
      // console.log(payload);
      this.friends = this.friends.filter((friend) => {
        return friend.name !== payload.name;
      });
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
