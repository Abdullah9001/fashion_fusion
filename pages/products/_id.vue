<template>
  <div>
    <template>
      <div class="product">
        <h1>{{ product.name }}</h1>
        <div class="cheap" v-for="(t, i) in product.tags" :key="i">
          <ul>
            <li>{{ t }}</li>
          </ul>
        </div>
        <img :src="product.image" :alt="product.name" />
        <p class="disc">{{ product.description }}</p>
        <div class="price">
          <p>Price: ${{ product.price }}</p>
          <p>Rating: {{ product.ratings }}</p>
        </div>

        <button>Add to Cart</button>
      </div>
    </template>
  </div>
</template>

<script>
export default {
  async created() {
    const p = await this.$content('products')
      .where({ id: parseInt(this.$route.params.id) })
      .limit(1)
      .fetch()
    this.product = p[0]
  },
  data() {
    return {
      product: null,
      product: {},
    }
  },
}
</script>

<style scoped>
.product {
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: center;
  justify-content: center;
  padding: 4rem;
}

li {
  list-style: none;
  color: #fff;
  font-family: 'Rubik', sans-serif;
}

img {
  width: 100%;
  max-width: 100%;
  object-fit: cover;
  border-radius: 5px;
  flex: 1;
  max-width: 500px;
  margin: 1rem 0;
}

.price {
  display: flex;
}

h1 {
  font-size: 24px;
  color: #fff;
  font-family: 'Rubik', sans-serif;
  font-size: 2rem;
  margin: 1rem 0;
}

p {
  margin-bottom: 10px;
  color: #fff;
  font-family: 'Rubik', sans-serif;
  margin: 0.5rem 1rem;
  font-size: 13px;
}
.disc {
  width: 600px;
}

button {
  padding: 10px 20px;
  margin: 1rem 0;
  font-family: 'Rubik', sans-serif;
  cursor: pointer;
}
</style>
