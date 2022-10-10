<template>
  <div class="flex flex-wrap items-center justify-center border-b-2 pb-3 border-orange-400">
    <ul class="flex items-center list-none text-xl font-thin font-sans">
        <nuxt-link to="/products"><li class="hover:underline underline-offset-8 decoration-orange-400" >Products</li></nuxt-link>
        <nuxt-link to="/"><li class="mx-8"><img src="../assets/img/bernis-logo.png" alt="" style="max-width: 280px" /></li></nuxt-link>
        <nuxt-link to="/contact"><li class="hover:underline underline-offset-8 decoration-orange-400">Contact</li></nuxt-link>
    </ul>

  </div>
</template>

<script>
export default {

}
</script>