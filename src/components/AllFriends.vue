<template>
  <div>
      All Friends
      <div v-for="(friend, index) of Totalfriends" :key="index">
          <p>{{friend.name}}</p>
      </div>
  </div>
</template>

<script>
export default {
    name: "AllFriends",
    props: ["Totalfriends"]
}
</script>

<style>

</style>