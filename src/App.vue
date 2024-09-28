<template>
<main-nav></main-nav>
<sub-nav></sub-nav>
<div class="wrapper">
  <div class="space"></div>
  <home></home>
  <div style="height: 200vh"></div>
</div>
</template>

<script>
import MainNav from "@/components/MainNav.vue";
import Home from "@/pages/Home.vue";
import SubNav from "@/components/SubNav.vue";
export default {
  components: {
    MainNav,
    Home,
  },

}
</script>

<style scoped>
.wrapper {
  height: auto;
}
.space {
  width: 100%;
  height: 7rem;
}
</style>
