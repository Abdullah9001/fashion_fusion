<template>
  <div>
    <div class="container">
      <div class="banner">
        <div class="banner-content1">
          <p>creazy deals</p>
          <h1>Buy 1 get 1 free</h1>
          <p>The best classic design in on sale at aj-shop</p>
          <NuxtLink to="/shop">Learn More</NuxtLink>
        </div>

        <div class="banner-content2">
          <p>spring/summer</p>
          <h1>Upcoming Season</h1>
          <p>The best classic design in on sale at aj-shop</p>
          <NuxtLink to="/shop">Collections</NuxtLink>
        </div>
      </div>
      <div class="banner">
        <div class="banner-text1">
          <h1>Seasonal Sale</h1>
          <h4>Winter Collection 50% Off</h4>
        </div>
        <div class="banner-text2">
          <h1>New Footwar Collections</h1>
          <h4>Spring / Summer 2022</h4>
        </div>
        <div class="banner-text3">
          <h1>T-Shirt</h1>
          <h4>New Trandy Shirt</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.container {
  padding: 3rem 0;
}

.banner {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 1rem 0;
}

.banner-content1 {
  background-image: url('/banner/b17.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  width: 41%;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 45vh;
}
.banner-content2 {
  background-image: url('/banner/b10.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  width: 43.5%;
  height: 300px;
  padding: 1rem;
  margin-left: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 45vh;
}

p {
  font-family: 'Rubik', sans-serif;
  color: #ffffff;
}

h1 {
  font-family: 'Rubik', sans-serif;
  color: #ffffff;
  word-spacing: 5px;
  margin-top: 5px;
}

a {
  font-family: 'Rubik', sans-serif;
  text-decoration: none;
  color: #ffffff;
  margin-top: 10px;
  padding: 7px;
  border: 1px solid #cccccc;
  width: 6.5rem;
  transition: 1s;
}

a:hover {
  background-color: #1cb0ba;
}

.banner-text1 {
  background-image: url('/banner/b7.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  width: 26.4%;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 25vh;
}
.banner-text2 {
  background-image: url('/banner/hero4.png');
  background-size: cover;
  background-repeat: no-repeat;
  width: 29%;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 25vh;
  margin-left: 1rem;
}
.banner-text3 {
  background-image: url('/banner/b18.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  width: 29%;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 25vh;
  margin-left: 1rem;
}
h4 {
  font-family: 'Rubik', sans-serif;
  color: #232121;
  margin-top: 5px;
}

@media (max-width: 884px) {
  h1 {
    font-size: 1rem;
  }
  h4 {
    font-size: 0.5rem;
  }
}

@media (max-width: 678px) {
  h1 {
    font-size: 1rem;
  }
  h4 {
    font-size: 0.8rem;
  }
}
</style>
