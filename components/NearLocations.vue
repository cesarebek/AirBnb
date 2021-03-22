<template>
  <div class="container mx-auto px-5 mt-9">
    <p class="text-3xl font-bold">Esplora i dintorni</p>
    <LocationsSlider class="md:hidden" :data="locations" />
    <div class="hidden md:block">
      <div class="my-5 grid md:grid-cols-3 lg:grid-cols-4 gap-4">
        <NearLocationCard
          v-for="location in locations"
          :key="location.city"
          :image="location.img"
          :city="location.city"
          :distance="location.time"
        />
      </div>
    </div>
  </div>
</template>

<script>
import NearLocationCard from '@/components/Home/NearLocationCard';
export default {
  components: { NearLocationCard },
  data() {
    return {
      locations: [
        {
          city: 'Verona',
          img:
            'https://a0.muscache.com/im/pictures/90dcb9c8-2e6a-4ce3-9acb-86d90d335314.jpg?im_q=medq&im_w=240',
          time: '3 ore in auto'
        },
        {
          city: 'Parma',
          img:
            'https://a0.muscache.com/im/pictures/560c06e1-a396-4414-9e38-4fbe8e9f04c4.jpg?im_q=medq&im_w=240',
          time: '4 ore in auto'
        },
        {
          city: 'Ponte di Legno',
          img:
            'https://a0.muscache.com/im/pictures/a7fe39da-3e57-44df-a744-9a73e482802d.jpg?im_q=medq&im_w=240',
          time: '4.5 ore in auto'
        },
        {
          city: 'Treviso',
          img:
            'https://a0.muscache.com/im/pictures/847cfb7f-788d-42dc-9148-f375348dde76.jpg?im_q=medq&im_w=240',
          time: '2 ore in auto'
        },
        {
          city: 'Perugia',
          img:
            'https://a0.muscache.com/im/pictures/ce6c498b-b069-401d-84c8-412bb4a4601e.jpg?im_q=medq&im_w=240',
          time: '6 ore in auto'
        },
        {
          city: 'Bibione',
          img:
            'https://a0.muscache.com/im/pictures/e8d3d6de-40b1-4341-89f2-afb2a1a4f71f.jpg?im_q=medq&im_w=240',
          time: '1.5 ore in auto'
        },
        {
          city: 'Brescia',
          img:
            'https://a0.muscache.com/im/pictures/676c0a60-2a5a-4598-aeeb-10a81aa5232f.jpg?im_q=medq&im_w=240',
          time: '3.5 ore in auto'
        },
        {
          city: 'La Spezia',
          img:
            'https://a0.muscache.com/im/pictures/a161fb95-6875-4aaa-aecd-3a46dead3220.jpg?im_q=medq&im_w=240',
          time: '5.5 ore in auto'
        }
      ]
    };
  }
};
</script>
