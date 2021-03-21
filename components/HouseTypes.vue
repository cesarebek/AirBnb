<template>
  <section class="container mx-auto my-5 px-5">
    <p class="text-3xl font-bold ">Una casa ovunque nel mondo</p>
    <div class="my-5 lg:flex gap-4 justify-between grid grid-cols-2">
      <BigCard
        v-for="house in houses"
        :key="house.type"
        :type="house.type"
        :image="house.img"
        :subtitle="''"
      />
    </div>
  </section>
</template>

<script>
import BigCard from '@/components/Home/BigCard';
export default {
  components: { BigCard },
  data() {
    return {
      houses: [
        {
          type: 'Case Intere',
          img:
            'https://a0.muscache.com/im/pictures/7d82ca14-56e5-4465-8218-dcfa7d69b6ac.jpg?im_w=480'
        },
        {
          type: 'Spazi unici',
          img:
            'https://a0.muscache.com/im/pictures/36f53e61-db8d-403c-9122-5b761c0e4264.jpg?im_w=480'
        },
        {
          type: 'Chalet e cottage',
          img:
            'https://a0.muscache.com/im/pictures/a596c528-a2e9-4417-9bbe-ceb68b2f6b9c.jpg?im_w=480'
        },
        {
          type: 'Animali domestici ammessi',
          img:
            'https://a0.muscache.com/im/pictures/10a638e1-6aff-4313-8033-1275cec83987.jpg?im_w=480'
        }
      ]
    };
  }
};
</script>
