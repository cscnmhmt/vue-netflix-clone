<template>
  <Header />
  <Banner
    title="Money Heist"
    description="To carry out the biggest heist in history, a mysterious man called The Professor recruits a band of eight robbers who have a single characteristic: n..."
  />
  <div v-for="feature in features" :key="features.id">
    <Feature :title="feature.title" :images="feature.images" />
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
import Header from './components/Header.vue';
import Banner from './components/Banner.vue';
import Feature from './components/Feature.vue';

export default {
  components: { Header, Banner, Feature },
  setup() {
    const features = ref([]);

    onMounted(async () => {
      try {
        const response = await fetch('./data.json');
        const data = await response.json();
        features.value = data.features;
      } catch (error) {
        console.error('Error fetching data:', error);
      }
    });

    return {
      features,
    };
  },
};
</script>

<style scoped></style>
