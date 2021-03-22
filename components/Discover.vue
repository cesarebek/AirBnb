<template>
  <section class="container mx-auto my-5 px-5">
    <p class="text-3xl font-bold ">Una casa ovunque nel mondo</p>
    <Slider class="md:hidden" :data="experiences" />
    <div class="hidden md:block">
      <div class="my-5 flex gap-4 justify-between">
        <BigCard
          v-for="experience in experiences"
          :key="experience.title"
          :type="experience.title"
          :image="experience.img"
          :subtitle="experience.subtitle"
        />
      </div>
    </div>
  </section>
</template>

<script>
import BigCard from '@/components/Home/BigCard';
export default {
  components: { BigCard },
  data() {
    return {
      experiences: [
        {
          title: 'Esperienze online',
          subtitle: 'Viaggia il mondo senza uscire di casa.',
          img:
            'https://a0.muscache.com/im/pictures/4d353c80-e73a-4b04-9e15-ec3d8381b106.jpg?im_w=480'
        },
        {
          title: 'Esperienze',
          subtitle: 'Attività a cui partecipare, ovunque sei.',
          img:
            'https://a0.muscache.com/im/pictures/e81fce5f-2f51-4342-938e-5bc18ae237f4.jpg?im_w=480'
        },
        {
          title: 'Avventure',
          subtitle: 'Gite di più giorni con vitto e alloggio.',
          img:
            'https://a0.muscache.com/im/pictures/b9adfc39-6e2a-4e5f-b6f3-681b306fae5c.jpg?im_w=480'
        }
      ]
    };
  }
};
</script>
