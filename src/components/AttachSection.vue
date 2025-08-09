<template>
  <section id="attach" class="mb-20">
    <div
      class="bg-gradient-to-br from-[#415E72]/40 to-[#17313E]/60 backdrop-blur-lg rounded-3xl p-8 border border-[#C5B0CD]/20 shadow-2xl"
    >
      <!-- Section Header -->
      <div class="text-center mb-8">
        <div
          class="inline-flex items-center justify-center w-16 h-16 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-2xl mb-4 shadow-lg"
        >
          <span class="text-2xl">🔗</span>
        </div>
        <h3
          class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-[#F3E2D4] to-[#C5B0CD] mb-2"
        >
          アタッチの使い方
        </h3>
        <div
          class="w-24 h-1 bg-gradient-to-r from-[#C5B0CD] to-[#F3E2D4] mx-auto rounded-full"
        ></div>
      </div>

      <div class="space-y-8">
        <!-- What is Attach -->
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
            アタッチって何？
          </h4>
          <p class="text-[#F3E2D4]/90 mb-6 leading-relaxed text-lg">
            アタッチとは、ゲームオブジェクトに「部品」を取り付けることです。
            車にエンジンを付けるような感じです。
          </p>
          <div
            class="bg-gradient-to-r from-[#C5B0CD]/20 to-[#F3E2D4]/20 p-6 rounded-xl border-l-4 border-[#C5B0CD] backdrop-blur-sm"
          >
            <div class="flex items-start space-x-3">
              <span class="text-3xl">🚗</span>
              <p class="text-[#F3E2D4]/90 leading-relaxed">
                車（ゲームオブジェクト）にエンジン（スクリプト）、ライト（Light）、
                音響（AudioSource）などの部品を付けて、ちゃんと動く車にします！
              </p>
            </div>
          </div>
        </div>

        <!-- Attach Methods -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#F3E2D4] to-[#C5B0CD] rounded-lg flex items-center justify-center mr-3 text-sm"
              >📝</span
            >
            アタッチの方法
          </h4>
          <div class="space-y-6">
            <div
              v-for="(method, index) in attachMethods"
              :key="index"
              class="bg-gradient-to-br from-[#415E72]/30 to-[#C5B0CD]/10 p-6 rounded-xl border border-[#C5B0CD]/20"
            >
              <h5 class="font-semibold text-[#F3E2D4] mb-4 flex items-center">
                <span
                  class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-full flex items-center justify-center text-[#17313E] font-bold text-sm mr-3"
                >
                  {{ index + 1 }}
                </span>
                {{ method.title }}
              </h5>
              <ol
                class="list-decimal list-inside space-y-2 text-[#F3E2D4]/80 pl-11"
              >
                <li v-for="step in method.steps" :key="step">{{ step }}</li>
              </ol>
            </div>
          </div>
        </div>

        <!-- Common Components -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#F3E2D4] to-[#C5B0CD] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🎯</span
            >
            よく使うコンポーネント
          </h4>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-4">
            <div
              v-for="component in commonComponents"
              :key="component.name"
              class="group bg-gradient-to-br from-[#415E72]/40 to-[#C5B0CD]/20 p-4 rounded-xl border border-[#C5B0CD]/30 hover:border-[#C5B0CD]/50 transition-all duration-300 hover:scale-105"
            >
              <div class="flex items-center mb-2">
                <span class="text-2xl mr-3">{{ component.icon }}</span>
                <h5 class="font-semibold text-[#F3E2D4]">{{ component.name }}</h5>
              </div>
              <p class="text-[#F3E2D4]/80 text-sm">{{ component.description }}</p>
            </div>
          </div>
        </div>

        <!-- Pro Tip -->
        <div
          class="bg-gradient-to-r from-[#F3E2D4]/30 to-[#C5B0CD]/30 backdrop-blur-sm p-6 rounded-2xl border border-[#F3E2D4]/40"
        >
          <div class="flex items-start space-x-4">
            <div
              class="w-12 h-12 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-xl flex items-center justify-center flex-shrink-0"
            >
              <span class="text-xl">💡</span>
            </div>
            <div>
              <h5 class="font-bold text-[#F3E2D4] mb-2">🦍 猿ポイント</h5>
              <p class="text-[#F3E2D4]/90 leading-relaxed">
                アタッチしたコンポーネントは、Inspectorで右クリック→「Remove
                Component」で外せます。
                いろいろ試してみて、不要になったら外しましょう！
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
  name: "AttachSection",
  data() {
    return {
      attachMethods: [
        {
          title: "Add Componentボタン",
          steps: [
            "Hierarchyでオブジェクトを選択",
            "Inspectorの「Add Component」ボタンをクリック",
            "追加したいコンポーネントを検索して選択",
          ],
        },
        {
          title: "ドラッグ&ドロップ",
          steps: [
            "Projectからスクリプトファイルを選択",
            "Inspectorにドラッグ&ドロップ",
            "または、Hierarchyのオブジェクトにドラッグ",
          ],
        },
      ],
      commonComponents: [
        { name: "Rigidbody", icon: "⚡", description: "物理演算（重力など）" },
        { name: "Collider", icon: "🛡️", description: "当たり判定" },
        { name: "AudioSource", icon: "🔊", description: "音を鳴らす" },
        { name: "Animator", icon: "🎭", description: "アニメーション制御" },
        { name: "Light", icon: "💡", description: "照明" },
        { name: "Script", icon: "📜", description: "プログラム（C#）" },
      ],
    };
  },
};
</script>
