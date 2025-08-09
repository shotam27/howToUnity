<template>
  <div
    class="min-h-screen bg-gradient-to-br from-dark-navy via-medium-blue/30 to-dark-navy"
  >
    <!-- Background Effects -->
    <div class="fixed inset-0 pointer-events-none">
      <div
        class="absolute top-0 left-0 w-96 h-96 bg-light-purple/10 rounded-full blur-3xl"
      ></div>
      <div
        class="absolute top-1/2 right-0 w-64 h-64 bg-cream/10 rounded-full blur-3xl"
      ></div>
      <div
        class="absolute bottom-0 left-1/3 w-80 h-80 bg-medium-blue/20 rounded-full blur-3xl"
      ></div>
    </div>

    <!-- Main Content -->
    <div class="relative z-10">
      <Navigation />

      <main class="max-w-6xl mx-auto px-4 py-8">
        <HeroSection />
        <PrefabSection />
        <AttachSection />
        <UIToolkitSection />
        <TipsSection />
      </main>

      <Footer />
    </div>
  </div>
</template>

<script>
import Navigation from "./components/Navigation.vue";
import HeroSection from "./components/HeroSection.vue";
import PrefabSection from "./components/PrefabSection.vue";
import AttachSection from "./components/AttachSection.vue";
import UIToolkitSection from "./components/UIToolkitSection.vue";
import TipsSection from "./components/TipsSection.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Navigation,
    HeroSection,
    PrefabSection,
    AttachSection,
    UIToolkitSection,
    TipsSection,
    Footer,
  },
};
</script>
