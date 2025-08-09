<template>
  <section id="ui-toolkit" class="mb-20">
    <div
      class="bg-gradient-to-br from-[#415E72]/40 to-[#17313E]/60 backdrop-blur-lg rounded-3xl p-8 border border-[#C5B0CD]/20 shadow-2xl"
    >
      <!-- Section Header -->
      <div class="text-center mb-8">
        <div
          class="inline-flex items-center justify-center w-16 h-16 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-2xl mb-4 shadow-lg"
        >
          <span class="text-2xl">🎨</span>
        </div>
        <h3
          class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-[#F3E2D4] to-[#C5B0CD] mb-2"
        >
          Unity UI Toolkit + UI Builder
        </h3>
        <div
          class="w-24 h-1 bg-gradient-to-r from-[#C5B0CD] to-[#F3E2D4] mx-auto rounded-full"
        ></div>
      </div>

      <div class="space-y-8">
        <!-- What is UI Toolkit -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🤔</span
            >
            UI Toolkitって何？
          </h4>
          <p class="text-[#F3E2D4]/90 mb-6 leading-relaxed text-lg">
            UI
            Toolkitは、Unityでゲームの画面（UI）を作るための新しいシステムです。
            ボタンや文字、メニューなどを作るのに使います。
          </p>
          <div
            class="bg-gradient-to-r from-[#C5B0CD]/20 to-[#F3E2D4]/20 p-6 rounded-xl border-l-4 border-[#C5B0CD] backdrop-blur-sm"
          >
            <div class="flex items-start space-x-3">
              <span class="text-3xl">📱</span>
              <p class="text-[#F3E2D4]/90 leading-relaxed">
                スマホアプリの画面を作るような感じです。
                「スタートボタン」「設定メニュー」「スコア表示」などを配置します！
              </p>
            </div>
          </div>
        </div>

        <!-- How to Start -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🚀</span
            >
            UI Builderの始め方
          </h4>
          <div class="space-y-4">
            <div
              v-for="(step, index) in startSteps"
              :key="index"
              class="bg-[#415E72]/30 rounded-xl p-4 border border-[#C5B0CD]/20"
            >
              <div class="flex items-center mb-2">
                <span
                  class="w-8 h-8 bg-gradient-to-br from-[#F3E2D4] to-[#C5B0CD] rounded-full flex items-center justify-center text-[#17313E] font-bold text-sm mr-3"
                  >{{ index + 1 }}</span
                >
                <span class="text-[#F3E2D4] font-medium">{{ step }}</span>
              </div>
            </div>
          </div>
        </div>

        <!-- UI Builder Steps -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🏗️</span
            >
            UI Builderの使い方
          </h4>
          <div class="space-y-4">
            <div
              v-for="(step, index) in builderSteps"
              :key="index"
              class="bg-gradient-to-r from-[#415E72]/40 to-[#C5B0CD]/20 p-4 rounded-xl border border-[#C5B0CD]/30"
            >
              <h5 class="font-semibold text-[#F3E2D4] mb-2 flex items-center">
                <span
                  class="w-6 h-6 bg-gradient-to-br from-[#F3E2D4] to-[#C5B0CD] rounded-full flex items-center justify-center text-[#17313E] font-bold text-xs mr-3"
                >
                  {{ index + 1 }}
                </span>
                {{ step.title }}
              </h5>
              <p class="text-[#F3E2D4]/80 text-sm pl-9">
                {{ step.description }}
              </p>
            </div>
          </div>
        </div>

        <!-- UI Elements -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🧩</span
            >
            主なUI要素
          </h4>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-4">
            <div
              v-for="element in uiElements"
              :key="element.name"
              class="group bg-gradient-to-br from-[#415E72]/40 to-[#C5B0CD]/20 p-4 rounded-xl border border-[#C5B0CD]/30 hover:border-[#C5B0CD]/50 transition-all duration-300 hover:scale-105"
            >
              <div class="flex items-center mb-2">
                <span class="text-2xl mr-3">{{ element.icon }}</span>
                <h5 class="font-semibold text-[#F3E2D4]">{{ element.name }}</h5>
              </div>
              <p class="text-[#F3E2D4]/80 text-sm">{{ element.description }}</p>
            </div>
          </div>
        </div>

        <!-- Benefits -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-4 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >⭐</span
            >
            UI Toolkitの良いところ
          </h4>
          <div
            class="bg-gradient-to-r from-[#415E72]/40 to-[#F3E2D4]/20 p-6 rounded-xl border border-[#F3E2D4]/30"
          >
            <h5 class="font-semibold text-[#F3E2D4] mb-3">
              🦍 猿でもわかるメリット
            </h5>
            <div class="space-y-3">
              <ul class="space-y-2 text-[#F3E2D4]/80 text-sm">
                <li class="flex items-start">
                  <span class="w-2 h-2 bg-[#C5B0CD] rounded-full mr-2"></span>
                  軽くて速い（Canvasより高性能）
                </li>
                <li class="flex items-start">
                  <span class="w-2 h-2 bg-[#C5B0CD] rounded-full mr-2"></span>
                  ウェブ技術（HTML/CSS）と似てる
                </li>
                <li class="flex items-start">
                  <span class="w-2 h-2 bg-[#C5B0CD] rounded-full mr-2"></span>
                  エディター拡張にも使える
                </li>
                <li class="flex items-start">
                  <span class="w-2 h-2 bg-[#C5B0CD] rounded-full mr-2"></span>
                  再利用しやすい
                </li>
              </ul>
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
                UI
                Toolkitは最初難しく感じるかもしれませんが、CanvasよりもプロっぽいUIが作れます！
                ウェブサイト作りと似ているので、HTMLとCSSを知っていると楽になります。
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
  name: "UIToolkitSection",
  data() {
    return {
      startSteps: [
        "Window → UI Toolkit → UI Builder を開く",
        "新しいDocument(.uxml)を作成",
        "Library から要素をドラッグ&ドロップ",
        "Inspector で要素のプロパティを調整",
        "StyleSheet(.uss)でデザインを装飾",
      ],
      builderSteps: [
        {
          title: "プロジェクトでUI Documentを作成",
          description: "Assets/Create/UI Toolkit/UI Document",
        },
        {
          title: "UI Builderでレイアウト設計",
          description: "ボタンやラベルなどの要素を配置",
        },
        {
          title: "スタイルシートでデザイン",
          description: "色や大きさ、フォントなどを設定",
        },
        {
          title: "ゲームオブジェクトにアタッチ",
          description: "UI DocumentコンポーネントをCanvasに追加",
        },
        {
          title: "スクリプトで動作制御",
          description: "ボタンクリックなどのイベントを処理",
        },
      ],
      uiElements: [
        {
          name: "Button",
          icon: "🔘",
          description: "クリックできるボタン",
        },
        {
          name: "Label",
          icon: "📝",
          description: "テキストを表示",
        },
        {
          name: "TextField",
          icon: "📝",
          description: "入力できるテキスト欄",
        },
        {
          name: "Image",
          icon: "🖼️",
          description: "画像を表示",
        },
        {
          name: "Slider",
          icon: "🎚️",
          description: "数値を調整するスライダー",
        },
        {
          name: "Toggle",
          icon: "☑️",
          description: "オン・オフを切り替え",
        },
        {
          name: "ScrollView",
          icon: "📜",
          description: "スクロールできる領域",
        },
        {
          name: "ListView",
          icon: "📋",
          description: "リスト形式で項目を表示",
        },
        {
          name: "ProgressBar",
          icon: "📊",
          description: "進捗を表示するバー",
        },
      ],
    };
  },
};
</script>
