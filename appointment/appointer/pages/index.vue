<template>
  <div>
    <nav class="bg-white">
      <div class="max-w-7xl mx-auto px-4">
        <div class="flex items-center justify-between h-16">
          <div class="flex items-center">
            <!-- Logo with image -->
            <a href="/" class="flex items-center">
              <img src="../assets/images/logo.png" alt="Logo" class="h-8 w-auto mr-2">
              <span class="text-pink-600 font-bold text-lg">Appointer</span>
            </a>
          </div>
          <div class="hidden md:block">
            <div class="flex space-x-4">
              <!-- Navigation links -->
              <a href="#" class="text-gray-800 hover:text-pink-600 font-medium">About Us</a>
              <a href="#" class="text-gray-800 hover:text-pink-600 font-medium">Services</a>
              <a href="#" class="text-gray-800 hover:text-pink-600 font-medium">Our Doctors</a>
              <a href="#" class="text-gray-800 hover:text-pink-600 font-medium">Appointment</a>
              <a href="#" class="text-gray-800 hover:text-pink-600 font-medium">Contact</a>
            </div>
          </div>
          <div class="hidden md:block">
            <div class="flex space-x-4">
              <!-- Login and Register links -->
              <a href="/log-in" class="text-gray-400 hover:text-pink-600 font-medium">Login</a>
              <a href="/register" class="text-gray-400 hover:text-pink-600 font-medium">Register</a>
            </div>
          </div>
        </div>
      </div>
    </nav>

    <div class="bg-cover bg-center h-screen relative" :style="`background-image: url(${bgImage})`">
      <!-- Background overlay -->
      <div class="absolute inset-0 bg-black opacity-50"></div>

      <!-- Main content -->
      <div class="flex items-center justify-center h-screen relative z-10">
        <div class="text-center">
          <h1 class="text-5xl font-bold text-gray-100 font-serif">Welcome to Appointer</h1>
          <br>
          <h2 class="text-2xl font-semibold text-gray-300 mb-8 font-serif">Find the right doctor and book an appointment</h2>
        </div>
      </div>
    </div>

    <div class="fixed bottom-4 right-4">
      <!-- Book appointment button with arrow -->
      <a href="#" class="inline-flex items-center justify-center bg-pink-500 hover:bg-pink-600 text-white py-2 px-4 rounded-full text-sm font-semibold space-x-1">
        <span>Book an Appointment</span>
        <svg class="h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
          <path fill-rule="evenodd" d="M11 16a.997.997 0 0 1-.707-.293l-5-5a.999.999 0 1 1 1.414-1.414L11 13.586l4.293-4.293a.999.999 0 1 1 1.414 1.414l-5 5A.997.997 0 0 1 11 16z" />
        </svg>
      </a>
    </div>
  </div>
</template>

<script>
import bgImage from '~/assets/images/bg-image4.jpg';

export default {
  data() {
    return {
      bgImage: '',
    };
  },
  mounted() {
    this.bgImage = bgImage;
  },
};
</script>

<style>
.bg-white {
  background-color: #ffffff;
}

.text-gray-800 {
  color: #2d3748;
}

.hover\:text-gray-600:hover {
  color: #4a5568;
}

.bg-pink-500 {
  background-color: #ed64a6;
}

.hover\:bg-pink-600:hover {
  background-color: #d53f8c;
}
</style>
