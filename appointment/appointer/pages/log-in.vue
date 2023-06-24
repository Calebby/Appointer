<template>
  <div class="bg-cover bg-center min-h-screen flex items-center justify-center" :style="`background-image: url(${bgImage})`">
    <div class="bg-white p-8 rounded shadow-md">
      <h1 class="text-2xl font-bold mb-4">Login</h1>
      <form>
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="email">Email</label>
          <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none" type="email" id="email" placeholder="Enter your email">
        </div>
        <div class="mb-6">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="password">Password</label>
          <input class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none" type="password" id="password" placeholder="Enter your password">
        </div>
        <div class="flex items-center justify-between">
          <button class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 rounded focus:outline-none focus:shadow-outline" type="button" @click="login">Login</button>
        </div>
        <div class="mt-4 text-center">
          <a class="text-blue-600 hover:underline" href="#">Forgot Password?</a>
        </div>
        <div class="flex justify-center mt-6">
          <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-6 rounded focus:outline-none focus:shadow-outline mr-2" type="button" @click="redirectToFacebookLogin">
            Facebook
          </button>
          <button class="bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-6 rounded focus:outline-none focus:shadow-outline" type="button" @click="redirectToGoogleLogin">
            Google
          </button>
        </div>
        <div class="text-center mt-6">
          <p class="text-gray-700 text-sm">Don't have an account? <a class="text-blue-600 hover:underline" href="/register">Create New Account</a></p>
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
    login() {
      // Handle login logic
    },
    redirectToFacebookLogin() {
      const facebookLoginUrl = 'https://www.facebook.com/';
      window.open(facebookLoginUrl, 'https://www.facebook.com/');
    },
    redirectToGoogleLogin() {
      const googleLoginUrl = 'hhttps://accounts.google.com/InteractiveLogin/identifier?continue=https%3A%2F%2Fmail.google.com%2Fmail%2Fu%2F0%2F&emr=1&followup=https%3A%2F%2Fmail.google.com%2Fmail%2Fu%2F0%2F&osid=1&passive=1209600&service=mail&ifkv=Af_xneEkk9AomaV4Hza3sMD4ggSKokS7pX7D3qAwN89EBw9qyUjFb9OliXvBAdIyrMzf5cZGYzpk0w&flowName=GlifWebSignIn&flowEntry=ServiceLoginttps://accounts.google.com/InteractiveLogin/signinchooser?continue=https%3A%2F%2Fmail.google.com%2Fmail%2Fu%2F0%2F&emr=1&followup=https%3A%2F%2Fmail.google.com%2Fmail%2Fu%2F0%2F&osid=1&passive=1209600&service=mail&ifkv=Af_xneEkk9AomaV4Hza3sMD4ggSKokS7pX7D3qAwN89EBw9qyUjFb9OliXvBAdIyrMzf5cZGYzpk0w&flowName=GlifWebSignIn&flowEntry=ServiceLogin';
      window.open(googleLoginUrl, '_blank');
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

.text-red-600 {
  color: #ef4444;
}

.text-red-600:hover {
  color: #dc2626;
}

.hover\:underline:hover {
  text-decoration: underline;
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
</style>
