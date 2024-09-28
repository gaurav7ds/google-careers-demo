<template>
  <header>
    <nav>
      <div class="left">
        <div class="hamburger">
          <div class="line"></div>
          <div class="line"></div>
          <div class="line"></div>
        </div>
        <div class="logo">
          <p>
            <span class="blue">G</span>
            <span class="red">o</span>
            <span class="yellow">o</span>
            <span class="blue">g</span>
            <span class="green">l</span>
            <span class="red">e</span> <span class="grey">Careers</span>
          </p>
        </div>
        <div class="links">
          <a href="">Teams</a>
          <a href="">Locations</a>
          <a href="">Benefits</a>
          <a href="">Jobs</a>
          <a href="">Students</a>
        </div>
      </div>
      <div class="right">
        <p>Gaurav Suhag</p>
      </div>
    </nav>
    <sub-nav></sub-nav>
  </header>
</template>

<script>
import SubNav from './SubNav.vue';
export default {
  components:{
    SubNav
  },
};
</script>

<style scoped>
header {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 200;
  background: white;
}
nav {
  padding: 1.8rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 0.06rem solid var(--color-grey-2);
}
.logo p {
  font-size: 2.1rem;
  font-weight: 500;
  cursor: pointer;
}
.left {
  display: flex;
  align-items: center;
}
.links a {
  font-size: 1.5rem;
  color: var(--color-grey-2);
  text-decoration: none;
  outline: none;
  margin-left: 3rem;
  cursor: pointer;
}
.hamburger {
  width: 2rem;
  height: 1.4rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  margin-right: 2rem;
  cursor: pointer;
}
.line {
  width: 100%;
  height: 0.2rem;
  border-radius: 2rem;
  background-color: var(--color-grey-2);
}
.right {
  margin-right: 3rem;
}
.right p {
  font-size: 1.7rem;
  color: var(--color-grey-2);
}
</style>