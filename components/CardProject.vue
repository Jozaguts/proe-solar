<template>
  <div class="max-w-sm rounded overflow-hidden shadow-lg">
    <img class="w-full" :src="data.src" :alt="data.alt" />
    <div class="px-6 py-4">
      <div class="font-bold text-xl mb-2" v-text="data.title"></div>
      <p class="text-gray-700 text-base" v-text="data.description"></p>
    </div>
    <div class="px-6 py-4">
      <span
        class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2"
        v-for="tag in data.tags" :key="tag"
        v-text="tag"
        ></span
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardProject',
  props: ['data']
}
</script>

<style scoped></style>
