<template>
  <div class="hero">
    <Hero />
    <HeroProduct :products="products" />
    <Features />
    <Banner />
    <NewsLetter />
  </div>
</template>

<script>
import Banner from '~/components/Banner.vue'
import Features from '~/components/Features.vue'
export default {
  components: { Features, Banner },
  name: 'IndexPage',
  async created() {
    this.products = await this.$content('products')
      .where({ onSale: true })
      .fetch()
  },
  data() {
    return {
      products: null,
    }
  },
}
</script>
