<template>
  <div id="app">
   <AllFriends :Totalfriends="friends" />
   <OnlineFriends :Totalfriends="friends" />
  
  </div>
</template>

<script>
import AllFriends from "./components/AllFriends"
import OnlineFriends from "./components/OnlineFriends"
export default {
  name: 'App',
  components: {
    AllFriends,
    OnlineFriends
  },
  data(){
    return{
      friends: [
        {name:'Mario', online: true},
        {name:'Luigi', online: false},
        {name:'Todd', online: true},
        {name:'Bowzer', online: false}
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
