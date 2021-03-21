<template>
  <div class="flex text-gray-900 cursor-pointer">
    <div class="h-28 w-28 overflow-hidden mr-3 rounded-xl">
      <img :src="image" alt="location" />
    </div>
    <div class="flex flex-col justify-center space-y-1 flex-auto">
      <h2 class="font-semibold text-lg">{{ city }}</h2>
      <h3>{{ distance }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  props: ['image', 'city', 'distance']
};
</script>
