<template>
    <div class="bg-cover bg-center min-h-screen flex items-center justify-center" :style="`background-image: url(${bgImage})`">
      <div class="bg-white p-8 rounded shadow-md w-96">
        <h1 class="text-2xl font-bold mb-4">Registration</h1>
        <form>
          <div class="mb-4">
            <label class="block text-gray-700 text-sm font-bold mb-2" for="firstName">First Name</label>
            <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none" type="text" id="firstName" placeholder="Enter your first name">
          </div>
          <div class="mb-4">
            <label class="block text-gray-700 text-sm font-bold mb-2" for="lastName">Last Name</label>
            <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none" type="text" id="lastName" placeholder="Enter your last name">
          </div>
          <div class="mb-4">
            <label class="block text-gray-700 text-sm font-bold mb-2" for="age">Age</label>
            <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none" type="number" id="age" placeholder="Enter your age">
          </div>
          <div class="mb-4">
            <label class="block text-gray-700 text-sm font-bold mb-2" for="email">Email or Phone number</label>
            <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none" type="text" id="email" placeholder="Enter your email or phone number">
          </div>
          <div class="flex items-center justify-between">
            <button class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 rounded focus:outline-none focus:shadow-outline" type="button" @click="register">Register</button>
          </div>
          <div class="mt-4 text-center">
            <a class="text-blue-600 hover:underline" href="#">Having trouble logging in? Click here.</a>
          </div>
        </form>
      </div>
    </div>
  </template>
  
  <script>
  import bgImage from '~/assets/images/bg-image.jpg';
  
  export default {
    data() {
      return {
        bgImage: '',
      };
    },
    mounted() {
      this.bgImage = bgImage;
    },
    methods: {
      register() {
        // Handle registration logic
      },
    },
  };
  </script>
  
  <style scoped>
  .bg-cover {
    background-repeat: no-repeat;
  }
  
  .bg-center {
    background-position: center;
  }
  
  .bg-white {
    background-color: #ffffff;
  }
  
  .text-gray-700 {
    color: #4a5568;
  }
  
  .text-blue-600 {
    color: #3b82f6;
  }
  
  .text-blue-600:hover {
    color: #2563eb;
  }
  
  .border-gray-300 {
    border-color: #e5e7eb;
  }
  
  .rounded {
    border-radius: 0.25rem;
  }
  
  .shadow-md {
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  }
  
  .focus\:outline-none:focus {
    outline: none;
    box-shadow: 0 0 0 2px rgba(156, 163, 175, 0.5);
  }
  
  .focus\:shadow-outline:focus {
    box-shadow: 0 0 0 3px rgba(66, 153, 225, 0.5);
  }
  
  .hover\:underline:hover {
    text-decoration: underline;
  }
  </style>
  