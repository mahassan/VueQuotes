<template>
  <div>
      Online Friends
      <div v-for="(friends, index) in Totalfriends" :key="index">
          <p  @click="toggleStatus(friends.name)" v-if="friends.online">{{friends.name}}</p>
          <!-- <span class="pill">online</span> -->
      </div>
  </div>
</template>

<script>
export default {
    props:["Totalfriends"],
    methods: {
        toggleStatus(friend){
            this.$emit("toggleStatus",{friend})
        }
    }
}
</script>

<style>

</style>