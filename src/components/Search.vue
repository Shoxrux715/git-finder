<template>
  <div class="search">
    <div class="search__box">
      <div class="search__input">
        <input
          placeholder="Введите имя пользователя"
          class="search__box-input"
          v-model="search"
          @keydown.enter="getUserInfo"
        />
        <button class="search__input-btn" @click="clear">❌</button>
      </div>
    </div>
    <button @click="getUserInfo" class="search__btn">НАЙТИ</button>
  </div>
</template>

<script>
import { mapActions, mapMutations } from "vuex";
export default {
  data() {
    return {
      search: "",
    };
  },
  methods: {
    ...mapActions(["userInfo"]),
    ...mapMutations(["resetUser"]),
    getUserInfo() {
      this.userInfo(this.search);
    },
    clear() {
      this.search = "";
      this.resetUser()
    },
  },
};
</script>

<style>
</style>