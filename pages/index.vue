<template>
  <div class="hero">
    <Hero />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async created() {
    this.sale_items = await this.$content('products')
      .where({ onSale: true })
      .fetch()
    this.products = await this.$content('products').fetch()
  },
  data() {
    return {
      products: null,
      sale_items: null,
    }
  },
}
</script>
