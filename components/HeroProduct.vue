<template>
  <div id="hero-products">
    <div class="product-text">
      <h1>Some Of Our Product</h1>
    </div>
    <div class="cards">
      <div
        class="product-card"
        v-for="(p, i) in products"
        :key="`hotProduct-${i}`"
      >
        <NuxtLink :to="`/products/${p.id}`">
          <div class="container">
            <img :src="p.image" alt="product-image" />
          </div>
          <div class="details">
            <h3>{{ p.name }}</h3>
            <h5>{{ p.price }}</h5>
            <div class="cheap">
              <div v-for="(t, i) in p.tags" :key="`prod-${p.id}-${i}`">
                <li>{{ t }}</li>
              </div>
            </div>
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    products: Array,
  },
}
</script>

<style scoped>
a {
  text-decoration: none;
}
#hero-products {
  align-items: center;
  justify-content: center;
  padding: 4rem;
}

.product-text {
  display: flex;
  flex-direction: column;
  text-align: center;
  padding: 20px;
}

h1 {
  color: #fff;
  font-size: 2rem;
  font-family: 'Rubik', sans-serif;
}
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  padding: 20px;
  grid-gap: 40px;
}

.product-card {
  background-color: #1c1b29;
  border-radius: 20px;
  box-shadow: 0 0 30px rgb(0, 0, 0, 0.18);
  cursor: pointer;
  filter: drop-shadow(15px 26px 22px #000);
}

.container {
  z-index: -1000;
  clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
}

.details {
  padding: 20px 10px;
}

.details > h3 {
  color: #fff;
  font-family: 'Rubik', sans-serif;
  font-weight: bold;
  font-size: 18px;
  margin: 10px 0 15px 0;
}

.details > h5 {
  color: #a0a0a0;
  font-size: 15px;
  font-weight: 400;
  margin: 10px 0;
}

.cheap {
  display: flex;
}
li {
  list-style: none;
  padding: 5px 8px;
  color: #fff;
  border: 1px solid #323030;
  font-family: 'Rubik', sans-serif;
  margin-right: 5px;
  font-size: 10px;
  border-radius: 20px;
}

img {
  width: 100%;
  height: 200px;
  display: block;
  object-fit: cover;
  border-radius: 20px 20px 0 0;
  z-index: -100;
}
</style>
