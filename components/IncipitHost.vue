<template>
  <div class="container mx-auto px-5">
    <div class="relative my-5 overflow-hidden rounded-2xl">
      <div
        class="md:absolute top-0 bg-black md:bg-transparent h-full flex flex-col justify-center w-full md:w-1/2 lg:w-1/3 text-white space-y-5 p-10 text-center md:text-left"
      >
        <h1 class="text-3xl font-bold">
          Il tuo mondo merita di essere condiviso
        </h1>
        <p>Trasforma lo spazio in più in una nuova opportunità.</p>
        <div>
          <button
            class="bg-white rounded-lg p-2 px-4 font-semibold text-gray-500 "
          >
            Diventa host
          </button>
        </div>
      </div>
      <div
        class="screen-2 bg-cover bg-right bg-repeat-none md:hidden"
        :style="{
          backgroundImage: `url(https://a0.muscache.com/im/pictures/eff28e1d-51c4-49ff-8266-68d6929ea1ec.jpg?im_w=1200)`
        }"
      ></div>
      <img
        class="hidden md:block"
        src="https://a0.muscache.com/im/pictures/eff28e1d-51c4-49ff-8266-68d6929ea1ec.jpg?im_w=1680"
        alt="discover"
      />
    </div>
  </div>
</template>
