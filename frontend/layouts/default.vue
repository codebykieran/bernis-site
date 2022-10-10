<template>
    <div class="container mx-auto py-3">
        <navigation></navigation>
        <Nuxt />
    </div>
</template>

<script>
import navigation from '../components/navigation.vue'
export default {
  components: { navigation },

}
</script>