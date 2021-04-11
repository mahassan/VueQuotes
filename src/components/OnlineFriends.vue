<template>
  <div>
      Online Friends
      <div v-for="(friends, index) in Totalfriends" :key="index">
          <p v-if="friends.online">{{friends.name}}</p>
      </div>
  </div>
</template>

<script>
export default {
    props:["Totalfriends"]
}
</script>

<style>

</style>