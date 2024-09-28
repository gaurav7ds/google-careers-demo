<template>
  <div class="sub-nav">
    <div class="left">
        <i class="material-icons">search</i>
        <div class="found">823</div>
        <p>jobs matched</p>
    </div>
    <div class="right">
        <div class="saved">Saved Jobs</div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.sub-nav {
    padding: 1.8rem;
    border-bottom: 0.06rem solid var(--color-grey-2);
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.left{
    display: flex;
    align-items: center;
    font-size: 1.5rem;
    color: var(--color-grey-2);
    margin-left: 2rem;
}
.found{
    margin: 0 .7rem 0 1rem;
    color: var(--color-green-2);
    font-weight: 600;
    font-size: 1.6rem;
}
.right{
    font-size: 1.5rem;
    color: var(--color-grey-2);
    margin-right: 4rem;
}
</style>