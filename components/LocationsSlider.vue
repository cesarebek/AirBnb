<template>
  <client-only>
    <section class="container mx-auto overflow-hidden my-5">
      <Hooper style="height: auto" :settings="hooperSettings">
        <Slide v-for="(loc, index) in data" :index="index" :key="loc.city">
          <NearLocationCard
            class="m-1"
            :city="loc.city"
            :distance="loc.time"
            :image="loc.img"
          />
        </Slide>
      </Hooper>
    </section>
  </client-only>
</template>

<script>
import NearLocationCard from '@/components/Home/NearLocationCard.vue';
export default {
  components: { NearLocationCard },
  props: ['data'],
  data() {
    return {
      hooperSettings: {
        trimWhiteSpace: true,
        itemsToShow: 1.3,
        breakpoints: {
          640: {
            itemsToShow: 2.3
          }
        }
      }
    };
  }
};
</script>
