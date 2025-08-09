<template>
  <!-- TailwindCSS 動作確認バー -->
  <div class="bg-green-500 text-white text-center py-2 text-sm font-bold">
    ✅ TailwindCSS 正常動作中 - この緑のバーが表示されていればCSS読み込み成功
  </div>
  
  <div
    class="min-h-screen bg-gradient-to-br from-[#17313E] via-[#415E72]/30 to-[#17313E] overflow-x-hidden"
  >
    <!-- Enhanced Background Effects -->
    <div class="fixed inset-0 pointer-events-none">
      <div
        class="absolute top-0 left-0 w-96 h-96 bg-[#C5B0CD]/10 rounded-full blur-3xl animate-float"
      ></div>
      <div
        class="absolute top-1/2 right-0 w-64 h-64 bg-[#F3E2D4]/10 rounded-full blur-3xl animate-float"
        style="animation-delay: 2s"
      ></div>
      <div
        class="absolute bottom-0 left-1/3 w-80 h-80 bg-[#415E72]/20 rounded-full blur-3xl animate-float"
        style="animation-delay: 1s"
      ></div>

      <!-- Additional floating elements -->
      <div
        class="absolute top-1/4 left-1/2 w-32 h-32 bg-[#C5B0CD]/5 rounded-full blur-2xl animate-float"
        style="animation-delay: 3s"
      ></div>
      <div
        class="absolute bottom-1/4 right-1/4 w-48 h-48 bg-[#F3E2D4]/5 rounded-full blur-3xl animate-float"
        style="animation-delay: 4s"
      ></div>
    </div>

    <!-- Main Content -->
    <div class="relative z-10">
      <Navigation />

      <main class="max-w-7xl mx-auto px-6 py-12">
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
