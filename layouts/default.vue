<template>
  <div>
    <header class="header-container">
      <div class="header-content">
        <h1 class="header-title">Happy Birthday</h1>
      </div>
    </header>
    <div class="nav-wrapper">
      <nav class="nav-links">
        <nuxt-link to="/" class="nav-link">HOner</nuxt-link>
        <nuxt-link to="/about" class="nav-link">About</nuxt-link>
        <nuxt-link to="/account" class="nav-link">Account</nuxt-link>
        <nuxt-link to="/themes" class="nav-link">Themes</nuxt-link>
        <nuxt-link to="/contact" class="nav-link">Contact Us</nuxt-link>
      </nav>
    </div>
  </div>
</template>

<script setup>
  // Any additional script can go here
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Italianno&family=Inter:wght@400;700&display=swap');

.header-container {
  background-color: #094037;
  border-top: 4px solid #F3CB60;
  padding: 20px;
  text-align: center;
}

.header-title {
  color: #F3CB60;
  font-size: 3rem;
  font-family: 'Italianno', cursive;
  margin: 0;
}

.nav-wrapper {
  background-color: #F3CB60;
  padding: 5px 10px; /* Reduce padding for a more compact design */
  border-radius: 0 0 30px 30px;
  margin-top: -20px;
  width: fit-content;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  justify-content: center;
}

.nav-links {
  display: flex;
  justify-content: space-around;
  gap: 10px; /* Reduce gap between links */
}

.nav-link {
  color: #05705F;
  padding: 8px 16px; /* Adjust padding for more compact links */
  border-radius: 10px;
  font-family: 'Inter', sans-serif;
  font-weight: bold;
  text-transform: uppercase;
  transition: background-color 0.3s, color 0.3s;
}

.nav-link:hover {
  background-color: #05705F;
  color: #F3CB60;
}
</style>
