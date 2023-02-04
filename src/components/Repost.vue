<template>
  <div class="repos">
    <Repositem 
    v-for="repos in getReposSort" 
    :key="repos.id"
    :repos="repos"
    />
  </div>
</template>

<script>
import Repositem from "@/components/Repositem.vue";
import { mapGetters } from "vuex";
export default {
  components: {
    Repositem,
  },
  computed:{
    ...mapGetters(['getReposSort'])
  }
};
</script>

<style>
</style>