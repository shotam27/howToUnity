<template>
  <section id="tips" class="mb-20">
    <div
      class="bg-gradient-to-br from-[#415E72]/40 to-[#17313E]/60 backdrop-blur-lg rounded-3xl p-8 border border-[#C5B0CD]/20 shadow-2xl"
    >
      <!-- Section Header -->
      <div class="text-center mb-8">
        <div
          class="inline-flex items-center justify-center w-16 h-16 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-2xl mb-4 shadow-lg"
        >
          <span class="text-2xl">💡</span>
        </div>
        <h3
          class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-[#F3E2D4] to-[#C5B0CD] mb-2"
        >
          役立つ豆知識・コツ
        </h3>
        <div
          class="w-24 h-1 bg-gradient-to-r from-[#C5B0CD] to-[#F3E2D4] mx-auto rounded-full"
        ></div>
      </div>

      <div class="space-y-8">
        <!-- Game Development Basics -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🎮</span
            >
            ゲーム開発の基本
          </h4>
          <div class="grid md:grid-cols-2 gap-4">
            <div
              v-for="concept in gameBasics"
              :key="concept.name"
              class="bg-gradient-to-br from-[#415E72]/40 to-[#C5B0CD]/20 p-4 rounded-xl border border-[#C5B0CD]/30"
            >
              <div class="flex items-center mb-3">
                <span class="text-2xl mr-3">{{ concept.icon }}</span>
                <h5 class="font-semibold text-[#F3E2D4]">{{ concept.name }}</h5>
              </div>
              <p class="text-[#F3E2D4]/80 text-sm leading-relaxed">
                {{ concept.description }}
              </p>
            </div>
          </div>
        </div>

        <!-- Important Concepts -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >💡</span
            >
            知っておくと便利なポイント
          </h4>
          <div class="grid md:grid-cols-2 gap-4">
            <div
              v-for="concept in importantConcepts"
              :key="concept.name"
              class="bg-gradient-to-br from-[#415E72]/40 to-[#C5B0CD]/20 p-4 rounded-xl border border-[#C5B0CD]/30"
            >
              <div class="flex items-center mb-2">
                <span class="text-2xl mr-3">{{ concept.icon }}</span>
                <h5 class="font-semibold text-[#F3E2D4]">{{ concept.name }}</h5>
              </div>
              <p class="text-[#F3E2D4]/80 text-sm leading-relaxed">
                {{ concept.description }}
              </p>
            </div>
          </div>
        </div>

        <!-- Keyboard Shortcuts -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >⌨️</span
            >
            便利なショートカットキー
          </h4>
          <div class="grid md:grid-cols-2 gap-6">
            <div class="space-y-3">
              <h5 class="text-[#F3E2D4] font-semibold mb-3 flex items-center">
                <span class="text-lg mr-2">⚡</span>
                基本操作
              </h5>
              <div
                v-for="shortcut in basicShortcuts"
                :key="shortcut.key"
                class="flex justify-between items-center p-3 bg-[#415E72]/30 rounded-lg border border-[#C5B0CD]/20"
              >
                <span class="text-[#F3E2D4]/90 text-sm">{{
                  shortcut.description
                }}</span>
                <code
                  class="bg-[#C5B0CD]/20 text-[#F3E2D4] px-2 py-1 rounded text-xs font-mono"
                  >{{ shortcut.key }}</code
                >
              </div>
            </div>
            <div class="space-y-3">
              <h5 class="text-[#F3E2D4] font-semibold mb-3 flex items-center">
                <span class="text-lg mr-2">🎯</span>
                シーン操作
              </h5>
              <div
                v-for="shortcut in sceneShortcuts"
                :key="shortcut.key"
                class="flex justify-between items-center p-3 bg-[#415E72]/30 rounded-lg border border-[#C5B0CD]/20"
              >
                <span class="text-[#F3E2D4]/90 text-sm">{{
                  shortcut.description
                }}</span>
                <code
                  class="bg-[#C5B0CD]/20 text-[#F3E2D4] px-2 py-1 rounded text-xs font-mono"
                  >{{ shortcut.key }}</code
                >
              </div>
            </div>
          </div>
        </div>

        <!-- Performance Tips -->
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
            パフォーマンス向上のコツ
          </h4>
          <div class="space-y-4">
            <div
              v-for="tip in performanceTips"
              :key="tip.title"
              class="bg-gradient-to-r from-[#415E72]/40 to-[#C5B0CD]/20 p-4 rounded-xl border border-[#C5B0CD]/30"
            >
              <h5 class="font-semibold text-[#F3E2D4] mb-2 flex items-center">
                <span class="text-xl mr-2">{{ tip.icon }}</span>
                {{ tip.title }}
              </h5>
              <p class="text-[#F3E2D4]/80 text-sm leading-relaxed">
                {{ tip.description }}
              </p>
            </div>
          </div>
        </div>

        <!-- Debugging Tips -->
        <div
          class="bg-gradient-to-br from-[#17313E]/80 to-[#415E72]/20 rounded-2xl p-6 border border-[#C5B0CD]/10"
        >
          <h4
            class="text-2xl font-semibold text-[#C5B0CD] mb-6 flex items-center"
          >
            <span
              class="w-8 h-8 bg-gradient-to-br from-[#C5B0CD] to-[#F3E2D4] rounded-lg flex items-center justify-center mr-3 text-sm"
              >🐛</span
            >
            デバッグのコツ
          </h4>
          <div class="space-y-4">
            <div
              v-for="tip in debugTips"
              :key="tip.title"
              class="bg-gradient-to-r from-[#415E72]/40 to-[#C5B0CD]/20 p-4 rounded-xl border border-[#C5B0CD]/30"
            >
              <h5 class="font-semibold text-[#F3E2D4] mb-2 flex items-center">
                <span class="text-xl mr-2">{{ tip.icon }}</span>
                {{ tip.title }}
              </h5>
              <p class="text-[#F3E2D4]/80 text-sm leading-relaxed">
                {{ tip.description }}
              </p>
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
              <span class="text-xl">🎓</span>
            </div>
            <div>
              <h5 class="font-bold text-[#F3E2D4] mb-2">🦍 最終猿ポイント</h5>
              <p class="text-[#F3E2D4]/90 leading-relaxed">
                Unityは奥が深いツールですが、基本をしっかり覚えれば必ず上達します！
                毎日少しずつでも触って、楽しみながら学習を続けてください。
                分からないことがあったら、Unity公式ドキュメントやコミュニティで調べてみましょう！
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
  name: "TipsSection",
  data() {
    return {
      gameBasics: [
        {
          name: "ゲームループ",
          icon: "🔄",
          description:
            "ゲームは毎秒60回画面を更新します。Update()関数がそのタイミングで実行されます。",
        },
        {
          name: "座標系",
          icon: "📍",
          description:
            "X(横), Y(縦), Z(奥行き)の3つの軸で位置を表現します。右手座標系を使用。",
        },
        {
          name: "コンポーネント",
          icon: "🧩",
          description:
            "ゲームオブジェクトに機能を追加するパーツ。LEGOブロックのようなもの。",
        },
        {
          name: "プレハブ",
          icon: "📦",
          description:
            "テンプレート化されたオブジェクト。同じものを複数作る時に便利。",
        },
      ],
      importantConcepts: [
        {
          name: "Inspector",
          icon: "🔍",
          description: "選択したオブジェクトの詳細設定ができる重要なウィンドウ",
        },
        {
          name: "Transform",
          icon: "📐",
          description: "位置・回転・スケールを管理する必須コンポーネント",
        },
        {
          name: "Hierarchy",
          icon: "📋",
          description: "シーン内のオブジェクトの一覧と親子関係を表示",
        },
        {
          name: "Project",
          icon: "📁",
          description: "アセット（素材）を管理するフォルダビュー",
        },
        {
          name: "Scene",
          icon: "🎬",
          description: "ゲームの一場面。ステージやメニュー画面など",
        },
        {
          name: "Console",
          icon: "💬",
          description: "エラーやログメッセージを確認できる重要なツール",
        },
      ],
      basicShortcuts: [
        { key: "Ctrl + S", description: "保存" },
        { key: "Ctrl + Z", description: "元に戻す" },
        { key: "Ctrl + Y", description: "やり直し" },
        { key: "Ctrl + D", description: "複製" },
        { key: "Delete", description: "削除" },
        { key: "F", description: "選択オブジェクトにフォーカス" },
      ],
      sceneShortcuts: [
        { key: "W", description: "移動ツール" },
        { key: "E", description: "回転ツール" },
        { key: "R", description: "スケールツール" },
        { key: "Q", description: "ビューツール" },
        { key: "Space", description: "再生/停止" },
        { key: "Alt + マウス", description: "カメラ回転" },
      ],
      performanceTips: [
        {
          icon: "🎯",
          title: "オブジェクトプーリング",
          description:
            "弾丸などの大量生成オブジェクトは、削除せずに再利用すると処理が軽くなります。",
        },
        {
          icon: "🖼️",
          title: "テクスチャ最適化",
          description:
            "画像のサイズは2のべき乗（256, 512, 1024など）にすると効率的です。",
        },
        {
          icon: "📐",
          title: "ポリゴン数の管理",
          description:
            "3Dモデルは必要以上に細かくしないように。遠くのオブジェクトは簡素化を。",
        },
        {
          icon: "⚡",
          title: "Update()の最適化",
          description:
            "毎フレーム実行される処理は最小限に。重い処理はコルーチンで分散を。",
        },
      ],
      debugTips: [
        {
          icon: "🖨️",
          title: "Debug.Log()を活用",
          description:
            "変数の値や実行状況をConsoleに出力して、動作を確認しましょう。",
        },
        {
          icon: "🎯",
          title: "Gizmosで可視化",
          description:
            "見えない当たり判定や範囲をシーンビューで線や図形として表示できます。",
        },
        {
          icon: "⏸️",
          title: "ブレークポイント",
          description:
            "Visual Studioでコードの特定行で実行を一時停止して、詳細に調査できます。",
        },
        {
          icon: "📊",
          title: "Profilerで性能分析",
          description:
            "処理の重い部分を特定して、最適化のポイントを見つけられます。",
        },
      ],
    };
  },
};
</script>
