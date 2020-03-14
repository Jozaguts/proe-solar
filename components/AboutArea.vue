<template>
    <div class="container mx-auto">
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-2 xl:grid-cols-2">
        <div class="container mx-auto mb-4">
          <img :src="image.src" :alt="image.alt">
        </div>
      </div>
    </div>
</template>

<script>
  export default {
    name: 'AboutArea',
    props: ['image']
  }
</script>

<style scoped>

</style>
