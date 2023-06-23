<template>
  <div class="nav">
    <div class="navber">
      <h1><NuxtLink to="/">Fashion Fusion</NuxtLink></h1>
      <div class="navber-link">
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li><NuxtLink to="/about">About</NuxtLink></li>
        <li><NuxtLink to="/product">Product</NuxtLink></li>
        <li><NuxtLink to="/dashboard">Dashboard</NuxtLink></li>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.nav {
  background-color: #000000;
  position: -webkit-sticky;
  position: sticky;
  top: 0;
}
.navber {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: space-between;
  width: 1200px;
  margin: auto;
}

h1 {
  background: #13cfcf;
  background: repeating-radial-gradient(
    circle farthest-corner at center center,
    #13cfcf 0%,
    #cf87a8 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 2rem;
  letter-spacing: -2.3px;
}

.navber-link {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
}

li {
  list-style: none;
  padding: 1.5rem 1.5rem;
}

li a {
  font-size: 1rem;
  color: #fff;
  font-style: bold;
  font-family: Arial, Helvetica, sans-serif;
  font-weight: 600;
  text-decoration: none;
}
</style>
