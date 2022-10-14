<template>        
    <div class="w-full bg-white rounded-lg">
        <img class="rounded-lg object-cover h-96 w-full " :src="$config.BACKEND_URL + product.attributes.image.data.attributes.formats.medium.url" alt="product.name">
        <div class="py-5">
            <h5 class="mb-2 text-xl tracking-tight text-gray-900">{{ product.attributes.name }}</h5>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">{{ product.attributes.description }}</p>
            <a href="#" class="inline-flex items-center py-2 text-sm font-medium text-center hover:underline decoration-2 underline-offset-8 decoration-orange-400 rounded-lg">
                Shop Me
            </a>
        </div>
    </div>
</template>

<script>
export default {
    props: { 
        product: Object
    }
}
</script>
