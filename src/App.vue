<template>
  <div>
    <!-- Show loader when isLoading is true -->
    <WhatsappIcon/>
    <Loader v-if="isLoading" />
    <!-- Show the actual content when loading is complete -->
    <div v-else>
      <router-view />
    </div>
  </div>
</template>

<script>
import Loader from './components/Layout/Loader.vue';
import WhatsappIcon from './components/Layout/WhatsAppIcon.vue'

export default {
  name: "App",
  components: {
    Loader,
    WhatsappIcon
  },
  data() {
    return {
      isLoading: true, // Initial state: loading
    };
  },
  mounted() {
    // Simulate a loading delay
    setTimeout(() => {
      this.isLoading = false; // Set loading to false after 2 seconds
    }, 2000);
  },
};
</script>