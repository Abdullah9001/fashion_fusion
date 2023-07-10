<template>
  <div class="products">
    <div class="search">
      <input type="text" placeholder="Search" />
      <p>Categories</p>
      <div class="category" v-for="(c, i) in categories" :key="`category${i}`">
        <img class="c-img" :src="c.image" alt="category img" />
        <h4>{{ c.name }}</h4>
      </div>
    </div>
    <div class="product">
      <div class="cards">
        <div
          class="product-card"
          v-for="(p, i) in products"
          :key="`product-${i}`"
        >
          <NuxtLink :to="`/products/${p.id}`">
            <div class="container">
              <img class="p-img" :src="p.image" alt="product-image" />
            </div>
            <div class="details">
              <h3>{{ p.name }}</h3>
              <h5>{{ p.price }}</h5>
              <div class="cheap">
                <ul v-for="(t, i) in p.tags" :key="`prod-${p.id}-${i}`">
                  <li>
                    {{ t }}
                  </li>
                </ul>
              </div>
            </div>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async created() {
    this.categories = await this.$content('category').fetch()
    this.products = await this.$content('products').fetch()
  },
  data() {
    return {
      products: null,
      categories: null,
    }
  },
}
</script>

<style scoped>
a {
  text-decoration: none;
}
.products {
  padding: 0 2rem;
  display: flex;
}

.search {
  padding-right: 2rem;
  padding-top: 1rem;
}

input {
  width: 150px;
  height: 40px;
  padding-left: 20px;
  font-size: 20px;
  font-family: 'Rubik', sans-serif;
  outline: none;
  border: 0.9px solid #201e22;
  margin-bottom: 30px;
  border-radius: 5px;
  color: #000;
  background-color: #f8f8f8;
}

p {
  margin-bottom: 20px;
  color: #fff;
  font-family: 'Rubik', sans-serif;
}

.category {
  display: flex;
  text-align: center;
  align-items: center;
  padding: 9px;
  cursor: pointer;
  border: 0.2px solid;
  margin: 5px 0;
  transition: 1s ease;
  border-radius: 5px;
}

.category:hover {
  border: 0.2px solid #1eb8b8;
}

.c-img {
  width: 40px;
  height: 40px;
  margin-right: 20px;
  object-fit: cover;
  border-radius: 50%;
}

h4 {
  font-family: 'Rubik', sans-serif;
  color: #fff;
  font-weight: 100;
}

/* Card */

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
  grid-template-columns: auto auto auto;
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

.p-img {
  width: 100%;
  height: 200px;
  display: block;
  object-fit: cover;
  border-radius: 20px 20px 0 0;
  z-index: -100;
}
</style>
