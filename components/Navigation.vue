<template>
  <header class="shadow-md py-5 text-gray-900 relative">
    <SearchBar class="hidden lg:block inset-center" />

    <nav class="container mx-auto flex justify-between items-center px-2">
      <!-- Left Side -->
      <div class="flex items-center">
        <NuxtLink to="/">
          <img
            class="h-8 lg:hidden"
            src="~/assets/images/airbnb-1.png"
            alt=""
          />
        </NuxtLink>
        <NuxtLink to="/">
          <img
            class="h-8 hidden lg:block"
            src="~/assets/images/airbnb-2.png"
            alt=""
          />
        </NuxtLink>

        <SearchBar class="hidden md:block lg:hidden ml-6" />
      </div>

      <!-- Right Side -->
      <div class="flex flex-shrink-0">
        <button class="button p-3 px-5">Diventa un host</button>
        <button class="button flex items-center px-3">
          <span class="material-icons">language</span>
        </button>
        <div class="relative">
          <button
            @click="optionsOpen = !optionsOpen"
            class="flex items-center h-full w-20 justify-between border border-gray-300 px-3 rounded-full duration-200 hover:shadow-md focus:shadow-md ml-2"
          >
            <span class="material-icons text-gray-600">menu</span>
            <span class="material-icons text-gray-600">account_circle</span>
          </button>
          <div
            v-if="optionsOpen"
            class="origin-top-right absolute right-0 bg-white rounded-xl mt-2 shadow-md"
          >
            <ul class="w-64 text-sm py-2 space-y-2">
              <div class="border-b border-gray-300">
                <li>Registrati</li>
                <li class="mb-2">Accedi</li>
              </div>
              <li>Diventa un host</li>
              <li>Proponi un esperienza</li>
              <li>Assistenza</li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
import SearchBar from '@/components/Navigation/SearchBar';
export default {
  components: { SearchBar },
  data() {
    return {
      optionsOpen: false
    };
  }
};
</script>

<style lang="postcss" scoped>
.button {
  @apply rounded-full font-semibold text-sm hover:bg-gray-100;
}
li {
  @apply py-3 px-4 hover:bg-gray-100 cursor-pointer;
}
</style>
