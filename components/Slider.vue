<template>
  <section class="container mx-auto overflow-hidden my-5">
    <Hooper style="height: auto" :settings="hooperSettings">
      <Slide v-for="exp in data" :key="exp.title"
        ><BigCard
          class="m-1"
          :type="exp.title"
          :subtitle="exp.subtitle"
          :image="exp.img"
        />
      </Slide>
    </Hooper>
  </section>
</template>

<script>
import BigCard from '@/components/Home/BigCard';
export default {
  components: { BigCard },
  props: ['data'],
  data() {
    return {
      hooperSettings: {
        trimWhiteSpace: true,
        itemsToShow: 1.5,
        breakpoints: {
          640: {
            itemsToShow: 2.5
          },
          768: {
            itemsToShow: 3
          }
        }
      }
    };
  }
};
</script>
