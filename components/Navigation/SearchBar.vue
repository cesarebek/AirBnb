<template>
  <!-- Input Box -->
  <div class="relative">
    <input
      v-model="searchBox"
      type="text"
      class="border border-gray-300 p-3 px-6 pr-12 rounded-full focus:outline-none font-semibold text-sm duration-200 hover:shadow-md"
      placeholder="Inizia la ricerca"
    />
    <div class="absolute top-0 right-2 h-full flex items-center">
      <button
        class=" bg-red-400 h-8 w-8 rounded-full flex items-center justify-center text-white"
      >
        <span class="material-icons">search</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchBox: ''
    };
  }
};
</script>
