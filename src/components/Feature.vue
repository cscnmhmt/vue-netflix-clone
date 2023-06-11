<template>
  <div class="fetures">
    <h2>{{ title }}</h2>
    <div class="image-container">
      <img v-for="image in images" :src="image" :key="image" alt="Card Image" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false,
    },
    images: {
      type: Array,
      required: false,
    },
  },
};
</script>

<style scoped>
.feature {
  width: 100%;
  padding: 10px;
  margin: 10px;
}

.image-container {
  padding: 20px;
  display: flex;
  justify-content: space-between;
}

.image-container img {
  width: 100px;
  height: 100px;
  object-fit: cover;
}
</style>
