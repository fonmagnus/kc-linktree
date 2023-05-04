<template>
  <div class="p-4 w-96 bg-white border-2 border-black-2000 rounded-lg shadow-lg hover:translate-y-1">
    <a :href="url" target="_blank">
      <div class="font-mono text-l text-center font-semi-bold text-gray-800">{{ title }}</div>
      <div class="font-mono text-xs text-center text-gray-500">{{ description }}</div>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    url: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
a {
  text-decoration: none;
}
</style>