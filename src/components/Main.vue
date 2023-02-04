<template>
  <main class="main">
   <div class="container">
      <Search/>
      <h2 class="error" v-if="error">{{error}}</h2>
      <User/>
      <Repost/>
   </div>
  </main>
</template>

<script>
import Search from "@/components/Search.vue";
import User from "@/components/User.vue";
import Repost from "@/components/Repost.vue";
import { mapState } from "vuex";
export default {
components:{
   Search,
   User,
   Repost
},
computed:{
   ...mapState(['error'])
}
}
</script>

<style>

</style>