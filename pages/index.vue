<template>
  <Tutorial/>
</template>

<script>
export default {
  name: 'IndexPage',
  methods:{
    async getProducts(){
      const res = await this.$axios.$get("/api/store/products");
      console.log("products",res)
    }
  },
  async mounted(){
    await this.getProducts()
  }
}
</script>
