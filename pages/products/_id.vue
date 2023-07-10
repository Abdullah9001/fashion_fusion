<template>
  <div></div>
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
    }
  },
}
</script>

<style scoped></style>
