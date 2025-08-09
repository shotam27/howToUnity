<template>
  <nav
    class="bg-gradient-to-r from-[#415E72] to-[#17313E] shadow-2xl backdrop-blur-xl sticky top-0 z-50 border-b border-[#C5B0CD]/30 px-6 py-4"
  >
    <div class="max-w-7xl mx-auto">
      <div class="flex justify-between items-center h-16">
        <div class="flex items-center space-x-4">
          <div
            class="w-12 h-12 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-2xl flex items-center justify-center text-2xl shadow-xl animate-pulse-glow"
          >
            🦍
          </div>
          <h1
            class="text-2xl font-black text-transparent bg-clip-text bg-gradient-to-r from-[#F3E2D4] to-[#C5B0CD] tracking-tight"
          >
            猿でもわかるUnity取説
          </h1>
        </div>
        <div class="hidden md:flex items-center space-x-10">
          <a
            v-for="item in menuItems"
            :key="item.id"
            :href="item.href"
            class="relative text-[#F3E2D4]/80 hover:text-[#C5B0CD] transition-all duration-500 font-bold text-lg group px-4 py-2 rounded-xl hover:bg-[#C5B0CD]/10"
            @click="scrollToSection"
          >
            {{ item.label }}
            <span
              class="absolute -bottom-2 left-1/2 transform -translate-x-1/2 w-0 h-1 bg-gradient-to-r from-[#C5B0CD] to-[#F3E2D4] transition-all duration-500 group-hover:w-full rounded-full"
            ></span>
          </a>
        </div>
        <button
          @click="toggleMobileMenu"
          class="md:hidden p-3 rounded-2xl bg-[#C5B0CD]/20 text-[#F3E2D4] hover:bg-[#C5B0CD]/30 transition-all duration-300 shadow-lg"
        >
          <svg
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            ></path>
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div
      v-if="mobileMenuOpen"
      class="md:hidden bg-[#17313E]/95 backdrop-blur-xl border-t border-[#C5B0CD]/30"
    >
      <div class="px-6 py-6 space-y-4">
        <a
          v-for="item in menuItems"
          :key="item.id"
          :href="item.href"
          class="block text-[#F3E2D4]/80 hover:text-[#C5B0CD] transition-colors font-bold text-lg py-3 px-4 rounded-xl hover:bg-[#C5B0CD]/10"
          @click="closeMobileMenu"
        >
          {{ item.label }}
        </a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navigation",
  data() {
    return {
      mobileMenuOpen: false,
      menuItems: [
        { id: "prefab", href: "#prefab", label: "プレハブ" },
        { id: "attach", href: "#attach", label: "アタッチ" },
        { id: "ui-toolkit", href: "#ui-toolkit", label: "UI Toolkit" },
        { id: "tips", href: "#tips", label: "Tips" },
      ],
    };
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen;
    },
    closeMobileMenu() {
      this.mobileMenuOpen = false;
    },
    scrollToSection(e) {
      e.preventDefault();
      const target = document.querySelector(e.target.getAttribute("href"));
      if (target) {
        target.scrollIntoView({
          behavior: "smooth",
          block: "start",
        });
      }
      this.closeMobileMenu();
    },
  },
};
</script>
