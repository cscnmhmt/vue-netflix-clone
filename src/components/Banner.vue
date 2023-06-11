<template>
  <div class="banner">
    <h1 class="title">{{ title }}</h1>
    <div class="button-group">
      <a href="#">Play</a>
      <a href="#">My List</a>
    </div>
    <p class="description">
      {{ description }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
    description: {
      type: String,
    },
  },
};
</script>

<style scoped>
.banner {
  padding: 150px 20px;
  background: url(../assets/banner.jpg);
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.button-group {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1.5rem;
  max-width: fit-content;
}
a {
  background-color: rgba(51, 51, 51, 0.5);
  color: #fff;
  padding: 0.3rem 1.5rem;
  border-radius: 5px;
  cursor: pointer;
  transition: 0.2s;
}
a:hover {
  background-color: #fff;
  color: #000;
}
</style>
