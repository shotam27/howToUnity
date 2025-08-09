<template>
  <footer
    class="bg-gradient-to-br from-[#415E72] via-[#17313E] to-[#415E72] py-16 mt-32 border-t border-[#C5B0CD]/30 relative overflow-hidden"
  >
    <!-- Background decoration -->
    <div
      class="absolute inset-0 bg-gradient-to-t from-[#17313E] to-transparent"
    ></div>
    <div
      class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-[#C5B0CD] via-[#F3E2D4] to-[#C5B0CD]"
    ></div>

    <div class="max-w-6xl mx-auto px-8 relative z-10">
      <!-- Main Footer Content -->
      <div class="text-center mb-12">
        <div class="flex items-center justify-center space-x-4 mb-6">
          <div
            class="w-16 h-16 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-3xl flex items-center justify-center text-3xl shadow-2xl animate-pulse-glow"
          >
            🦍
          </div>
          <h3
            class="text-3xl font-black text-transparent bg-clip-text bg-gradient-to-r from-[#F3E2D4] to-[#C5B0CD] tracking-tight"
          >
            猿でもわかるUnity取説
          </h3>
        </div>
        <div
          class="w-48 h-1 bg-gradient-to-r from-[#C5B0CD] via-[#F3E2D4] to-[#C5B0CD] mx-auto rounded-full mb-8 shadow-lg"
        ></div>
        <p class="text-[#C5B0CD]/90 text-xl mb-6 font-medium">
          頑張れば誰でもゲームが作れます！
        </p>
        <p class="text-[#F3E2D4]/80 text-lg">一歩ずつ進んでいきましょう！</p>
      </div>

      <!-- Quick Links -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-6 mb-12">
        <a
          v-for="link in quickLinks"
          :key="link.id"
          :href="link.href"
          class="group bg-gradient-to-br from-[#415E72]/40 to-[#C5B0CD]/20 backdrop-blur-xl p-6 rounded-3xl border border-[#C5B0CD]/30 hover:border-[#C5B0CD]/60 transition-all duration-500 text-center hover:scale-105 hover:shadow-xl"
          @click="scrollToSection"
        >
          <div
            class="text-3xl mb-3 group-hover:scale-125 transition-transform duration-500 group-hover:rotate-12"
          >
            {{ link.icon }}
          </div>
          <span
            class="text-[#F3E2D4]/80 text-sm font-medium group-hover:text-[#C5B0CD] transition-colors duration-300"
          >
            {{ link.label }}
          </span>
        </a>
      </div>

      <!-- Encouragement Message -->
      <div
        class="bg-gradient-to-r from-[#C5B0CD]/30 to-[#F3E2D4]/30 backdrop-blur-xl rounded-3xl p-10 border border-[#C5B0CD]/40 mb-12 shadow-2xl relative overflow-hidden"
      >
        <!-- Background decoration -->
        <div
          class="absolute inset-0 bg-gradient-to-br from-[#C5B0CD]/10 to-[#F3E2D4]/10 rounded-3xl"
        ></div>

        <div class="text-center relative z-10">
          <div class="flex items-center justify-center mb-6">
            <div
              class="w-12 h-12 bg-gradient-to-br from-[#F3E2D4] to-[#C5B0CD] rounded-2xl flex items-center justify-center shadow-xl"
            >
              <span class="text-xl">🌟</span>
            </div>
          </div>
          <h4 class="text-[#F3E2D4] font-bold text-xl mb-4">最後に一言</h4>
          <p class="text-[#F3E2D4]/90 leading-relaxed text-lg">
            Unity学習は最初は難しく感じるかもしれませんが、<br />
            <strong class="text-[#C5B0CD]">継続は力なり</strong>です！<br />
            小さな成功を積み重ねて、素晴らしいゲームを作りましょう！
          </p>
        </div>
      </div>

      <!-- Copyright -->
      <div class="text-center text-[#C5B0CD]/60 text-sm">
        <p>© 2025 猿でもわかるUnity取説 - 学習目的で作成されています</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      quickLinks: [
        { id: "prefab", href: "#prefab", icon: "📦", label: "プレハブ" },
        { id: "attach", href: "#attach", icon: "🔗", label: "アタッチ" },
        {
          id: "ui-toolkit",
          href: "#ui-toolkit",
          icon: "🎨",
          label: "UI Toolkit",
        },
        { id: "tips", href: "#tips", icon: "💡", label: "Tips" },
      ],
    };
  },
  methods: {
    scrollToSection(e) {
      e.preventDefault();
      const target = document.querySelector(
        e.target.closest("a").getAttribute("href")
      );
      if (target) {
        target.scrollIntoView({
          behavior: "smooth",
          block: "start",
        });
      }
    },
  },
};
</script>
