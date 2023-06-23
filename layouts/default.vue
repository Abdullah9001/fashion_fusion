<template>
  <div>
    <Navber />
    <Nuxt class="all-page" />
    <Footer />
  </div>
</template>

<script>
export default {}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.all-page {
  background: rgb(2, 0, 36);
  background: linear-gradient(
    45deg,
    rgba(2, 0, 36, 1) 0%,
    rgba(35, 99, 64, 1) 0%,
    rgba(29, 26, 66, 1) 32%,
    rgba(9, 15, 36, 1) 43%,
    rgba(17, 16, 36, 1) 55%,
    rgba(62, 9, 57, 1) 78%,
    rgba(106, 157, 149, 1) 100%,
    rgba(0, 212, 255, 1) 100%
  );
}
</style>
