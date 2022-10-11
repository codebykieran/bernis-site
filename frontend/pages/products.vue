<template>
    <div>
        <div v-for="product in products" :key=product.id>
            {{ product.attributes.name }}
            {{ product.attributes.description }}
            {{ '£' + product.attributes.price }}
            <img :src="'http://localhost:1337' + product.attributes.image.data.attributes.formats.medium.url"/> 
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
