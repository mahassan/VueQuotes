<template>
  <div id="app">
   <AllFriends :Totalfriends="friends" @toggleStatus="toggleStatus(name)" />
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
  },
  methods: {
    toggleStatus(payload){
      console.log(payload)
      this.friends = [this.friends.filter((friend)=>{
        return friend.name !== payload.name
      })]
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
.pill{
  border: 1px solid lightgreen;
  color: lightgreen;
  padding:5px;
  border-radius: 5px;
}
</style>
