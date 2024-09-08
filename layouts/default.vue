<template>
  <div class="min-h-screen w-full md:w-[430px] mx-auto p-4 bg-cover bg-center animate-fade-in">
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

    <!-- Scrollable Image Section with hover effects -->
    <div class="overflow-auto flex gap-3 snap-x pt-4">
      <img class="w-[200px] h-[150px] snap-center hover:scale-105 transition-transform duration-300 ease-in-out"
        src="https://images.unsplash.com/photo-1540206351-d6465b3ac5c1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=320&h=160&q=80" />
      <img class="w-[200px] h-[150px] snap-center hover:scale-105 transition-transform duration-300 ease-in-out"
        src="https://images.unsplash.com/photo-1540206351-d6465b3ac5c1?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=320&h=160&q=80" />
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
// Script logic if needed
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Kaushan+Script&display=swap');

body {
  background-image: url('/img/ma.png');
  background-size: cover;
}

.day {
  font-family: 'Kaushan Script', cursive;
  color: white;
}

/* Custom Animations */
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
