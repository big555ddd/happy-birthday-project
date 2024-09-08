<template>
  <div class="min-h-screen w-full md:w-[430px] mx-auto p-4 bg-cover bg-center animate-fade-in background-container">
    <!-- Happy Birthday Section -->
    <div class="flex flex-col items-center justify-center pt-5 text-center animate-pulse">
      <div class="day text-[24px]">Happy</div>
      <div class="day text-[40px]">Birthday</div>
    </div>

    <!-- Bouncing Images Section -->
    <div class="flex justify-around pt-7 z-1">
      <div class="animate-bounce">
        <img class="w-[90px] h-[80px]" src="/img/Rectangle 162.png" alt="Rectangle 162">
        <img class="w-[90px] h-[80px]" src="/img/Group 5.png" alt="Group 5">
      </div>

      <div class="h-[300px] w-[150px] border-[2px]"></div>

      <div class="animate-bounce">
        <img class="w-[90px] h-[80px]" src="/img/Rectangle 162.png" alt="Rectangle 162">
        <img class="w-[90px] h-[80px]" src="/img/Group 5.png" alt="Group 5">
      </div>
    </div>

    <!-- 3D Image Carousel Section with auto-slide and controlled gaps -->
    <div class="carousel-container overflow-hidden flex justify-center pt-4">
      <div class="carousel">
        <div class="carousel-item" v-for="(image, index) in images" :key="index" :style="getRotationStyle(index)">
          <img :src="image" class="carousel-image" alt="carousel image" />
        </div>
      </div>
    </div>

    <!-- YouTube Video Section with fade in effect -->
    <div class="flex justify-center items-center py-4 animate-fade-in">
      <iframe width="298" height="169" src="https://www.youtube.com/embed/n26NXNYbQG8"></iframe>
    </div>

    <!-- Grid of Notes Section with hover effects -->
    <div class="grid grid-cols-3 gap-4">
      <!-- First row -->
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/lazy.png" alt="Lazy" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/isaac.png" alt="Isaac" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/ice.png" alt="Ice" />
      
      <!-- Second row -->
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/boss.png" alt="Boss" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/kapi.png" alt="Kapi" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/oliver.png" alt="Oliver" />

      <!-- Third row -->
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/fin.png" alt="Fin" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/sun.png" alt="Sun" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/kiw.png" alt="Kiw" />

      <!-- Fourth row -->
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/earth.png" alt="Earth" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/kasalong.png" alt="Kasalong" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/negan.png" alt="Negan" />

      <!-- Fifth row -->
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/bar.png" alt="Bar" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/few.png" alt="Few" />
      <img class="w-full hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/daja.png" alt="Daja" />

      <!-- Sixth row (with centered Sorry image) -->
      <div></div>
      <img class="w-full mx-auto hover:scale-105 transition-transform duration-300 ease-in-out" src="../img/Sorry.png" alt="Sorry" />
      <div></div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

// List of images for the 3D carousel
const images = [
  "https://images.unsplash.com/photo-1540206351-d6465b3ac5c1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=320&h=160&q=80",
  "https://images.unsplash.com/photo-1518770660439-4636190af475?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=320&h=160&q=80",
  "https://images.unsplash.com/photo-1521747116042-5a810fda9664?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=320&h=160&q=80",
  "https://images.unsplash.com/photo-1472214103451-9374bd1c798e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=320&h=160&q=80",
]

// Function to calculate the rotation for each image
const getRotationStyle = (index) => {
  const angle = (360 / images.length) * index
  return {
    transform: `rotateY(${angle}deg) translateZ(220px)`, // Reduced translateZ value to reduce gap
  }
}

// Auto-rotate carousel
onMounted(() => {
  const carousel = document.querySelector('.carousel')
  let angle = 0

  setInterval(() => {
    angle -= 1 // Rotate slowly
    carousel.style.transform = `rotateY(${angle}deg)`
  }, 30) // Adjust the speed of rotation
})
</script>

<style scoped>
/* Apply background to the container */
.background-container {
  background-image: url('/img/ma.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  min-height: 100vh; /* Ensure it covers the full height */
}

.day {
  font-family: 'Kaushan Script', cursive;
  color: white;
}

/* Styling for carousel container with perspective */
.carousel-container {
  perspective: 1000px;
  width: 100%;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

/* Carousel container that rotates */
.carousel {
  width: 400px;
  height: 300px;
  position: relative;
  transform-style: preserve-3d;
  transform: rotateY(0deg);
  transition: transform 1s;
}

/* Each carousel item */
.carousel-item {
  position: absolute;
  width: 220px; /* Reduced width to bring images closer */
  height: 150px;
  backface-visibility: hidden;
}

/* Images within the carousel */
.carousel-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.animate-fade-in {
  animation: fadeIn 1s ease-in-out;
}
</style>
