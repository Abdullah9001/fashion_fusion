<template>
  <div class="error-page">
    <div class="error-message">
      <h1 v-if="error.statusCode === 404">Page not found</h1>
      <h1 v-else>An error occurred</h1>
      <NuxtLink to="/">Home page</NuxtLink>
    </div>
    <div class="error-image">
      <img src="error-img.jpg" alt="error-image" />
    </div>
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'empty',
}
</script>

<style scoped>
.error-page {
  display: flex;
  margin: auto;
  background-color: #fff;
  align-items: center;
  justify-content: center;
  height: 100vh;
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

.error-message {
  margin-right: 2rem;
}

h1 {
  font-family: 'Roboto', sans-serif;
  font-size: 3rem;
  color: aquamarine;
  text-shadow: 2px 1px rgb(49, 111, 90);
  margin-block: 2rem;
}

a {
  color: #fff;
  padding: 0.4rem 2rem;
  background-color: rgb(0, 0, 0);
  border-radius: 50px 0 0 0;
  text-decoration: none;
  font-family: 'Rubik', sans-serif;
  font-weight: 500;
}

img {
  height: 300px;
  border: 25px solid #000000;
  border-radius: 50px 0 0 0;
}
</style>
