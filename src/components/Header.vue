<template>
  <header>
    <div class="logo">
      <img src="../assets/netflix-logo.png" alt="Netflix Logo" />
    </div>
    <div class="avatar">
      <img src="../assets/netflix-avatar.png" alt="" />
    </div>
  </header>
</template>

<script></script>

<style scoped>
header {
  position: fixed;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
}

.logo {
  max-width: 120px;
}

.avatar {
  max-width: 30px;
}
</style>
