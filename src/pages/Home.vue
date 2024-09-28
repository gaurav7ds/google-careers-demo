<template>
  <div class="content">
    <div class="left">
      <div class="text-anim">
        <div class="outer">
          <div class="inner">
            <p class="red">Build</p>
            <p class="green">Create</p>
            <p class="blue">Design</p>
            <p class="yellow">Code</p>
          </div>
        </div>
        <p class="for">for everyone</p>
        <div class="search-wrapper">
          <p>Find your next job at Google.</p>
          <div class="search">
            <div class="input-field">
              <p class="r">Role</p>
              <i class="material-icons">search</i>
              <input type="text" placeholder="Software engineer" />
            </div>
            <div class="input-field">
              <p class="r">Where?</p>
              <i class="material-icons">place</i>
              <input type="text" placeholder="Los Angles" />
            </div>
            <div class="btn">
                <p>Search</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="img-anim">
        <div class="img-container">
          <div class="img show">
            <img src="@/assets/hero_1_1x.png" alt="" />
          </div>
          <div class="img">
            <img src="@/assets/hero_2_1x.png" alt="" />
          </div>
          <div class="img">
            <img src="@/assets/hero_3_1x.png" alt="" />
          </div>
          <div class="img">
            <img src="@/assets/hero_4_1x.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const inner = document.querySelector(".inner");
    const imgs = [...document.querySelectorAll(".img-container .img")];
    let index = 0;
    setInterval(() => {
      index += 1;
      const p = [...document.querySelectorAll(".inner p")];
      imgs.forEach((i) => i.classList.remove("show"));
      imgs.forEach((img, idx) => {
        if (index > imgs.length - 1) {
          index = 0;
        }
        if (idx === index) {
          img.classList.add("show");
        }
      });
      inner.style.transition = "transform .2s";
      inner.style.transform = "translateY(-11rem)";
      setTimeout(() => {
        let pClone = p[0].cloneNode(true);
        p[0].remove();
        inner.appendChild(pClone);
        inner.style.transition = "none";
        inner.style.transform = "translateY(0rem)";
      }, 200);
    }, 4000);
  },
};
</script>

<style scoped>
.text-anim {
  padding: 1rem;
  margin-top: 4.3rem;
}
p.for {
  font-size: 8rem;
  font-weight: 700;
  color: black;
}
.outer {
  height: 11rem;
  overflow: hidden;
}
.inner {
  font-size: 8rem;
  font-weight: 700;
  display: flex;
  flex-direction: column;
  transition: transform 0.2s;
}
.content {
  width: 100%;
  padding: 5rem 12rem;
  display: flex;
  justify-content: space-between;
}
.left {
  width: 58%;
}
.right {
  width: 41%;
}
.img-container {
  width: 100%;
  position: relative;
  overflow: hidden;
}
.img {
  position: absolute;
  width: 100%;
  opacity: 0;
  left: 0;
  right: 0;
}
.img.show {
  position: static;
  opacity: 1;
  transition: opacity 0.3s;
}
.img img {
  width: 100%;
  object-fit: cover;
}
.search-wrapper {
  margin-top: 3rem;
  width: 100%;
}
.search-wrapper p {
  font-size: 3rem;
}
.search {
  display: flex;
  align-items: center;
  margin-top: 7rem;
}
.input-field{
    width: 43%;
    position: relative;
}
i{
    position: absolute;
    top: 53%;
    left: 1.3rem;
    font-size: 2.5rem;
    color: var(--color-grey-2);
}
.input-field p.r{
  font-size: 1.5rem;
  margin-left: 2rem;
}
.input-field input {
    margin-top: 1rem;
    width: 90%;
    outline: none;
    padding: 1.6rem 1rem 1.6rem 4.4rem;
    font-size: 1.7rem;
    border: .1rem solid var(--color-grey-2);
    border-radius: 100rem;
}
.btn{
align-self: end;
}
.btn p{
    background-color: var(--color-blue-1);
    color: white;
    font-size: 1.4rem;
    text-align: center;
    padding: 1.8rem 3rem;
    border-radius: 100rem;
    filter: brightness(1.1);
}
input:focus{
    box-shadow: inset 0 0 0 .13rem var(--color-blue-1);
}
</style>