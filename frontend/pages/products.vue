<template>
    <div class="flex flex-row flex-wrap">
        <div class="my-5 w-1/2 md:w-1/4 px-3" v-for="product in products" :key=product.id>
            <productCard :product="product" />            
        </div>
    </div>
</template>

<script>

export default {

    data() {
        return {
            products: []
        }
    },
    methods: {
        async fetchProducts() {
            const products = await this.$axios.$get(this.$config.API_URL + 'products?populate=*')
            this.products = products.data
        }
    },
    mounted() {
        this.fetchProducts()
    }
}

</script>
