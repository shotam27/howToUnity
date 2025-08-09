<template>
  <section id="prefab" class="mb-20">
    <div
      class="bg-gradient-to-br from-[#415E72]/40 to-[#17313E]/60 backdrop-blur-lg rounded-3xl p-8 border border-[#C5B0CD]/20 shadow-2xl"
    >
      <!-- Section Header -->
      <div class="text-center mb-8">
        <div
          class="inline-flex items-center justify-center w-16 h-16 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-2xl mb-4 shadow-lg"
        >
          <span class="text-2xl">📦</span>
        </div>
        <h3
          class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-[#F3E2D4] to-[#C5B0CD] mb-2"
        >
          プレハブの使い方
        </h3>
        <div
          class="w-24 h-1 bg-gradient-to-r from-[#C5B0CD] to-[#F3E2D4] mx-auto rounded-full"
        ></div>
      </div>

      <div class="space-y-8">
        <!-- What is Prefab -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-4 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🤔</span
            >
            プレハブって何？
          </h4>
          <p class="text-[#F3E2D4]/90 mb-6 leading-relaxed text-lg">
            プレハブとは、ゲームオブジェクトの「設計図」のことです。
            同じキャラクターや建物を何個も作りたい時に使います。
          </p>
          <div
            class="bg-gradient-to-r from-[#C5B0CD]/20 to-[#F3E2D4]/20 p-6 rounded-xl border-l-4 border-[#C5B0CD] backdrop-blur-sm"
          >
            <div class="flex items-start space-x-3">
              <span class="text-3xl">🍎</span>
              <p class="text-[#F3E2D4]/90 leading-relaxed">
                例えば、リンゴを100個ゲームに配置したい時、1個1個作るのは大変ですよね？
                プレハブを使えば、リンゴの「ひな形」を1個作って、それをコピーして100個作れます！
              </p>
            </div>
          </div>
        </div>

        <!-- How to Create -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-4 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >📝</span
            >
            プレハブの作り方
          </h4>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div
              v-for="(step, index) in creationSteps"
              :key="index"
              class="bg-[#415E72]/30 rounded-xl p-4 border border-[#C5B0CD]/20"
            >
              <div class="flex items-center mb-2">
                <span
                  class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-full flex items-center justify-center text-[#17313E] font-bold text-sm mr-3"
                >
                  {{ index + 1 }}
                </span>
                <span class="text-[#F3E2D4] font-medium">{{ step }}</span>
              </div>
            </div>
          </div>
        </div>

        <!-- How to Use -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-4 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🎯</span
            >
            プレハブの使い方
          </h4>
          <div class="grid md:grid-cols-2 gap-6">
            <div
              class="bg-gradient-to-br from-[#415E72]/40 to-[#C5B0CD]/20 p-6 rounded-xl border border-[#C5B0CD]/30"
            >
              <h5 class="font-semibold text-[#F3E2D4] mb-3 flex items-center">
                <span class="text-2xl mr-2">📍</span>
                配置する時：
              </h5>
              <p class="text-[#F3E2D4]/80">ProjectからHierarchyにドラッグ</p>
            </div>
            <div
              class="bg-gradient-to-br from-[#415E72]/40 to-[#F3E2D4]/20 p-6 rounded-xl border border-[#F3E2D4]/30"
            >
              <h5 class="font-semibold text-[#F3E2D4] mb-3 flex items-center">
                <span class="text-2xl mr-2">✏️</span>
                編集する時：
              </h5>
              <p class="text-[#F3E2D4]/80">プレハブをダブルクリック</p>
            </div>
          </div>
        </div>

        <!-- Pro Tip -->
        <div
          class="bg-gradient-to-r from-[#C5B0CD]/30 to-[#F3E2D4]/30 backdrop-blur-sm p-6 rounded-2xl border border-[#C5B0CD]/40"
        >
          <div class="flex items-start space-x-4">
            <div
              class="w-12 h-12 bg-gradient-to-br from-[#F3E2D4] to-[#C5B0CD] rounded-xl flex items-center justify-center flex-shrink-0"
            >
              <span class="text-xl">💡</span>
            </div>
            <div>
              <h5 class="font-bold text-[#F3E2D4] mb-2">🦍 猿ポイント</h5>
              <p class="text-[#F3E2D4]/90 leading-relaxed">
                プレハブを編集すると、そのプレハブから作られた全てのオブジェクトが一斉に変わります！
                100個のリンゴの色を一気に変えたい時などに便利です。
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "PrefabSection",
  data() {
    return {
      creationSteps: [
        "Hierarchyでゲームオブジェクトを作成（例：Cube）",
        "そのオブジェクトを好きなようにカスタマイズ",
        "ProjectウィンドウのAssetsフォルダにドラッグ&ドロップ",
        "🎉 完成！青いアイコンになったらプレハブです",
      ],
    };
  },
};
</script>
