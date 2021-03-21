<template>
  <div class="cursor-pointer">
    <div class="overflow-hidden rounded-xl mb-2">
      <img :src="image" alt="House" />
    </div>
    <p class="text-gray-900 font-semibold text-lg">{{ type }}</p>
    <p class="text-gray-900 text-sm">{{ subtitle }}</p>
  </div>
</template>

<script>
export default {
  props: ['image', 'type', 'subtitle']
};
</script>
