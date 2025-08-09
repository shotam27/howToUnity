<template>
  <section class="relative overflow-hidden py-24 px-6 lg:py-32 mb-24">
    <!-- Enhanced Background Effects -->
    <div
      class="absolute inset-0 bg-gradient-to-br from-[#17313E] via-[#415E72]/30 to-[#17313E]"
    ></div>

    <!-- Floating orbs with animations -->
    <div
      class="absolute top-20 left-20 w-40 h-40 bg-[#C5B0CD]/30 rounded-full blur-3xl animate-float"
    ></div>
    <div
      class="absolute top-40 right-32 w-32 h-32 bg-[#F3E2D4]/20 rounded-full blur-2xl animate-float"
      style="animation-delay: 1s"
    ></div>
    <div
      class="absolute bottom-20 left-1/3 w-48 h-48 bg-[#415E72]/25 rounded-full blur-3xl animate-float"
      style="animation-delay: 2s"
    ></div>

    <!-- Gradient overlay -->
    <div
      class="absolute inset-0 bg-gradient-radial from-transparent via-transparent to-[#17313E]/50"
    ></div>

    <div class="relative z-10 text-center max-w-6xl mx-auto">
      <!-- TailwindCSS テスト要素 -->
      <div class="bg-red-500 text-white p-4 mb-4 rounded-lg">
        TailwindCSS動作テスト: この要素が赤い背景で表示されていればTailwind正常動作中
      </div>
      
      <!-- Main Title with enhanced styling -->
      <div class="mb-16 animate-fade-in">
        <div
          class="inline-flex items-center justify-center w-20 h-20 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-2xl mb-8 shadow-xl animate-pulse-glow"
        >
          <span class="text-4xl">🦍</span>
        </div>
        <h1
          class="text-5xl md:text-7xl lg:text-8xl font-black text-transparent bg-clip-text bg-gradient-to-r from-[#F3E2D4] via-[#C5B0CD] via-[#F3E2D4] to-[#C5B0CD] mb-8 animate-scale-in leading-tight"
        >
          Unity超初心者ガイド
        </h1>
        <div class="flex justify-center mb-8">
          <div
            class="w-48 h-2 bg-gradient-to-r from-[#C5B0CD] via-[#F3E2D4] to-[#C5B0CD] rounded-full shadow-lg"
          ></div>
        </div>
      </div>

      <!-- Enhanced Subtitle -->
      <div class="mb-20 animate-slide-up" style="animation-delay: 0.3s">
        <p
          class="text-2xl md:text-3xl lg:text-4xl text-[#C5B0CD]/90 mb-6 font-light leading-relaxed"
        >
          猿でもわかるレベルで説明します！
        </p>
        <p class="text-lg md:text-xl text-[#F3E2D4]/80 font-medium">
          ✨ 一緒に頑張ろう！みんなでゲーム制作の世界を楽しもう！ ✨
        </p>
      </div>

      <!-- Enhanced CTA Cards -->
      <div
        class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-20 animate-slide-up"
        style="animation-delay: 0.6s"
      >
        <div
          v-for="(card, index) in ctaCards"
          :key="card.id"
          class="group relative bg-gradient-to-br from-[#415E72]/40 to-[#17313E]/60 backdrop-blur-xl rounded-3xl p-8 border border-[#C5B0CD]/30 shadow-2xl hover:shadow-[0_25px_50px_-12px_rgba(197,176,205,0.25)] transition-all duration-700 hover:scale-110 hover:border-[#C5B0CD]/60 cursor-pointer overflow-hidden"
          @click="scrollToSection(card.target)"
          :style="`animation-delay: ${0.8 + index * 0.2}s;`"
        >
          <!-- Card background glow -->
          <div
            class="absolute inset-0 bg-gradient-to-br from-[#C5B0CD]/10 to-[#F3E2D4]/5 opacity-0 group-hover:opacity-100 transition-opacity duration-600 rounded-3xl"
          ></div>

          <!-- Content -->
          <div class="relative z-10">
            <div
              class="text-4xl mb-6 group-hover:scale-125 transition-transform duration-600 group-hover:rotate-12"
            >
              {{ card.icon }}
            </div>
            <h3
              class="font-bold text-xl text-[#F3E2D4] mb-4 group-hover:text-[#C5B0CD] transition-colors duration-400"
            >
              {{ card.title }}
            </h3>
            <p
              class="text-[#C5B0CD]/80 text-sm leading-relaxed group-hover:text-[#F3E2D4]/90 transition-colors duration-400"
            >
              {{ card.description }}
            </p>
          </div>

          <!-- Hover overlay -->
          <div
            class="absolute inset-0 bg-gradient-to-t from-[#C5B0CD]/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-600 rounded-3xl"
          ></div>
        </div>
      </div>

      <!-- Enhanced Encouraging Message -->
      <div
        class="animate-slide-up max-w-4xl mx-auto"
        style="animation-delay: 1.2s"
      >
        <div
          class="bg-gradient-to-r from-[#C5B0CD]/30 to-[#F3E2D4]/30 backdrop-blur-xl rounded-3xl p-12 border border-[#C5B0CD]/40 shadow-2xl relative overflow-hidden"
        >
          <!-- Background pattern -->
          <div
            class="absolute inset-0 bg-gradient-to-br from-[#C5B0CD]/10 to-[#F3E2D4]/10 rounded-3xl"
          ></div>

          <!-- Content -->
          <div class="relative z-10">
            <div class="flex items-center justify-center mb-8">
              <div
                class="w-16 h-16 bg-gradient-to-br from-[#F3E2D4] to-[#C5B0CD] rounded-2xl flex items-center justify-center shadow-xl"
              >
                <span class="text-2xl">🌟</span>
              </div>
            </div>
            <h3 class="text-2xl md:text-3xl font-bold text-[#F3E2D4] mb-6">
              Unity学習への第一歩
            </h3>
            <p class="text-lg md:text-xl text-[#F3E2D4]/90 leading-relaxed">
              プログラミング未経験でも大丈夫！<br />
              <span class="font-semibold text-[#C5B0CD]">継続は力なり</span>で、
              <span class="font-semibold text-[#F3E2D4]">素晴らしいゲーム</span
              >を作りましょう！
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HeroSection",
  data() {
    return {
      ctaCards: [
        {
          id: "prefab-card",
          icon: "📦",
          title: "プレハブ",
          description: "オブジェクトの設計図を作ろう",
          target: "#prefab",
        },
        {
          id: "attach-card",
          icon: "🔗",
          title: "アタッチ",
          description: "部品を取り付けよう",
          target: "#attach",
        },
        {
          id: "ui-card",
          icon: "🎨",
          title: "UI Toolkit",
          description: "美しい画面を作ろう",
          target: "#ui-toolkit",
        },
        {
          id: "tips-card",
          icon: "💡",
          title: "Tips",
          description: "便利なコツを覚えよう",
          target: "#tips",
        },
      ],
    };
  },
  methods: {
    scrollToSection(target) {
      const element = document.querySelector(target);
      if (element) {
        element.scrollIntoView({
          behavior: "smooth",
          block: "start",
        });
      }
    },
  },
};
</script>
