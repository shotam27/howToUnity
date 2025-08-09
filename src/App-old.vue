<template>
  <div class="min-h-screen bg-dark-navy">
    <!-- ナビゲーション -->
    <nav class="bg-medium-blue shadow-lg">
      <div class="max-w-7xl mx-auto px-4">
        <div class="flex justify-between h-16">
          <div class="flex items-center">
            <h1 class="text-xl font-bold text-cream">
              🦍 猿でもわかるUnity取説
            </h1>
          </div>
          <div class="flex items-center space-x-6">
            <a
              href="#prefab"
              class="text-cream hover:text-light-purple transition-colors"
              >プレハブ</a
            >
            <a
              href="#attach"
              class="text-cream hover:text-light-purple transition-colors"
              >アタッチ</a
            >
            <a
              href="#ui-toolkit"
              class="text-cream hover:text-light-purple transition-colors"
              >UI Toolkit</a
            >
            <a
              href="#tips"
              class="text-cream hover:text-light-purple transition-colors"
              >Tips</a
            >
          </div>
        </div>
      </div>
    </nav>

    <!-- メインコンテンツ -->
    <main class="max-w-4xl mx-auto px-4 py-8">
      <!-- ヒーローセクション -->
      <section class="text-center mb-12">
        <h2 class="text-4xl font-bold text-cream mb-4">
          🎮 Unity超初心者ガイド
        </h2>
        <p class="text-lg text-light-purple">
          猿でもわかるレベルで説明します！一緒に頑張ろう！
        </p>
      </section>

      <!-- プレハブセクション -->
      <section id="prefab" class="mb-16">
        <div class="bg-medium-blue rounded-lg p-8 mb-8">
          <h3 class="text-3xl font-bold text-cream mb-6 flex items-center">
            📦 プレハブの使い方
          </h3>

          <div class="space-y-6">
            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🤔 プレハブって何？
              </h4>
              <p class="text-cream mb-4">
                プレハブとは、ゲームオブジェクトの「設計図」のことです。
                同じキャラクターや建物を何個も作りたい時に使います。
              </p>
              <div
                class="bg-medium-blue p-4 rounded border-l-4 border-light-purple"
              >
                <p class="text-cream">
                  🍎
                  例えば、リンゴを100個ゲームに配置したい時、1個1個作るのは大変ですよね？
                  プレハブを使えば、リンゴの「ひな形」を1個作って、それをコピーして100個作れます！
                </p>
              </div>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                📝 プレハブの作り方
              </h4>
              <ol class="list-decimal list-inside space-y-3 text-cream">
                <li>Hierarchyでゲームオブジェクトを作成（例：Cube）</li>
                <li>そのオブジェクトを好きなようにカスタマイズ</li>
                <li>ProjectウィンドウのAssetsフォルダにドラッグ&ドロップ</li>
                <li>🎉 完成！青いアイコンになったらプレハブです</li>
              </ol>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🎯 プレハブの使い方
              </h4>
              <div class="grid md:grid-cols-2 gap-4">
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">配置する時：</h5>
                  <p class="text-cream text-sm">
                    ProjectからHierarchyにドラッグ
                  </p>
                </div>
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">編集する時：</h5>
                  <p class="text-cream text-sm">プレハブをダブルクリック</p>
                </div>
              </div>
            </div>

            <div class="bg-light-purple bg-opacity-20 p-4 rounded">
              <p class="text-cream">
                💡 <strong>猿ポイント：</strong>
                プレハブを編集すると、そのプレハブから作られた全てのオブジェクトが一斉に変わります！
                100個のリンゴの色を一気に変えたい時などに便利です。
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- アタッチセクション -->
      <section id="attach" class="mb-16">
        <div class="bg-medium-blue rounded-lg p-8 mb-8">
          <h3 class="text-3xl font-bold text-cream mb-6 flex items-center">
            🔗 アタッチの使い方
          </h3>

          <div class="space-y-6">
            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🤔 アタッチって何？
              </h4>
              <p class="text-cream mb-4">
                アタッチとは、ゲームオブジェクトに「部品」を取り付けることです。
                車にエンジンを付けるような感じです。
              </p>
              <div
                class="bg-medium-blue p-4 rounded border-l-4 border-light-purple"
              >
                <p class="text-cream">
                  🚗
                  車（ゲームオブジェクト）にエンジン（スクリプト）、ライト（Light）、
                  音響（AudioSource）などの部品を付けて、ちゃんと動く車にします！
                </p>
              </div>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                📝 アタッチの方法
              </h4>
              <div class="space-y-4">
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">
                    方法1: Add Componentボタン
                  </h5>
                  <ol
                    class="list-decimal list-inside space-y-1 text-cream text-sm"
                  >
                    <li>Hierarchyでオブジェクトを選択</li>
                    <li>Inspectorの「Add Component」ボタンをクリック</li>
                    <li>追加したいコンポーネントを検索して選択</li>
                  </ol>
                </div>

                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">
                    方法2: ドラッグ&ドロップ
                  </h5>
                  <ol
                    class="list-decimal list-inside space-y-1 text-cream text-sm"
                  >
                    <li>Projectからスクリプトファイルを選択</li>
                    <li>Inspectorにドラッグ&ドロップ</li>
                    <li>または、Hierarchyのオブジェクトにドラッグ</li>
                  </ol>
                </div>
              </div>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🎯 よく使うコンポーネント
              </h4>
              <div class="grid md:grid-cols-2 gap-4">
                <div class="space-y-3">
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Rigidbody</h5>
                    <p class="text-cream text-sm">物理演算（重力など）</p>
                  </div>
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Collider</h5>
                    <p class="text-cream text-sm">当たり判定</p>
                  </div>
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">AudioSource</h5>
                    <p class="text-cream text-sm">音を鳴らす</p>
                  </div>
                </div>
                <div class="space-y-3">
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Animator</h5>
                    <p class="text-cream text-sm">アニメーション制御</p>
                  </div>
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Light</h5>
                    <p class="text-cream text-sm">照明</p>
                  </div>
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Script</h5>
                    <p class="text-cream text-sm">プログラム（C#）</p>
                  </div>
                </div>
              </div>
            </div>

            <div class="bg-light-purple bg-opacity-20 p-4 rounded">
              <p class="text-cream">
                💡 <strong>猿ポイント：</strong>
                アタッチしたコンポーネントは、Inspectorで右クリック→「Remove
                Component」で外せます。
                いろいろ試してみて、不要になったら外しましょう！
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- UI Toolkitセクション -->
      <section id="ui-toolkit" class="mb-16">
        <div class="bg-medium-blue rounded-lg p-8 mb-8">
          <h3 class="text-3xl font-bold text-cream mb-6 flex items-center">
            🎨 Unity UI Toolkit + UI Builderの使い方
          </h3>

          <div class="space-y-6">
            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🤔 UI Toolkitって何？
              </h4>
              <p class="text-cream mb-4">
                UI
                Toolkitは、Unityでゲームの画面（UI）を作るための新しいシステムです。
                ボタンや文字、メニューなどを作るのに使います。
              </p>
              <div
                class="bg-medium-blue p-4 rounded border-l-4 border-light-purple"
              >
                <p class="text-cream">
                  📱 スマホアプリの画面を作るような感じです。
                  「スタートボタン」「設定メニュー」「スコア表示」などを配置します！
                </p>
              </div>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🚀 UI Builderの起動方法
              </h4>
              <ol class="list-decimal list-inside space-y-2 text-cream">
                <li>Unityのメニューバーから「Window」をクリック</li>
                <li>「UI Toolkit」を選択</li>
                <li>「UI Builder」をクリック</li>
                <li>🎉 UI Builderが開きます！</li>
              </ol>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                📝 基本的な使い方
              </h4>
              <div class="space-y-4">
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">
                    1. 新しいUIドキュメントを作成
                  </h5>
                  <p class="text-cream text-sm">
                    Project → 右クリック → Create → UI Toolkit → UI Document
                  </p>
                </div>

                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">
                    2. UI Builderで開く
                  </h5>
                  <p class="text-cream text-sm">
                    作成したUIドキュメントをダブルクリック
                  </p>
                </div>

                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">3. 要素を追加</h5>
                  <p class="text-cream text-sm">
                    左のLibraryからVisualElementやButtonをドラッグ&ドロップ
                  </p>
                </div>
              </div>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🎯 よく使うUI要素
              </h4>
              <div class="grid md:grid-cols-2 gap-4">
                <div class="space-y-3">
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Button</h5>
                    <p class="text-cream text-sm">クリックできるボタン</p>
                  </div>
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Label</h5>
                    <p class="text-cream text-sm">文字を表示</p>
                  </div>
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">TextField</h5>
                    <p class="text-cream text-sm">文字入力欄</p>
                  </div>
                </div>
                <div class="space-y-3">
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Image</h5>
                    <p class="text-cream text-sm">画像を表示</p>
                  </div>
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">VisualElement</h5>
                    <p class="text-cream text-sm">基本的な箱（コンテナ）</p>
                  </div>
                  <div class="bg-medium-blue p-3 rounded">
                    <h5 class="font-semibold text-cream">Slider</h5>
                    <p class="text-cream text-sm">スライダー（音量調整など）</p>
                  </div>
                </div>
              </div>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🎨 スタイリング
              </h4>
              <div class="bg-medium-blue p-4 rounded">
                <h5 class="font-semibold text-cream mb-2">
                  CSSのように装飾できます：
                </h5>
                <ul class="list-disc list-inside space-y-1 text-cream text-sm">
                  <li>背景色、文字色の変更</li>
                  <li>フォントサイズ、太さの調整</li>
                  <li>余白（margin、padding）の設定</li>
                  <li>角丸（border-radius）の設定</li>
                  <li>影（box-shadow）の追加</li>
                </ul>
              </div>
            </div>

            <div class="bg-light-purple bg-opacity-20 p-4 rounded">
              <p class="text-cream">
                💡 <strong>猿ポイント：</strong>
                UI BuilderはWebサイト作成のような感覚で使えます。
                慣れるまで時間がかかりますが、一度覚えると圧倒的に効率的です！
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- その他のTipsセクション -->
      <section id="tips" class="mb-16">
        <div class="bg-medium-blue rounded-lg p-8 mb-8">
          <h3 class="text-3xl font-bold text-cream mb-6 flex items-center">
            💡 その他有用な知識
          </h3>

          <div class="space-y-6">
            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🎮 ゲーム開発の基本
              </h4>
              <div class="grid md:grid-cols-2 gap-4">
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">Scene（シーン）</h5>
                  <p class="text-cream text-sm">
                    ゲームの「ステージ」や「画面」のこと。タイトル画面、ゲーム画面、結果画面など
                  </p>
                </div>
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">GameObject</h5>
                  <p class="text-cream text-sm">
                    ゲーム内の「物」。キャラクター、建物、カメラなど全て
                  </p>
                </div>
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">Transform</h5>
                  <p class="text-cream text-sm">
                    位置、回転、大きさの情報。全てのGameObjectに付いている
                  </p>
                </div>
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">Component</h5>
                  <p class="text-cream text-sm">
                    GameObjectに機能を追加する「部品」
                  </p>
                </div>
              </div>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                ⌨️ 便利なショートカットキー
              </h4>
              <div class="grid md:grid-cols-2 gap-4">
                <div class="space-y-2">
                  <div class="flex justify-between bg-medium-blue p-2 rounded">
                    <span class="text-cream">Ctrl + S</span>
                    <span class="text-light-purple text-sm">保存</span>
                  </div>
                  <div class="flex justify-between bg-medium-blue p-2 rounded">
                    <span class="text-cream">Ctrl + Z</span>
                    <span class="text-light-purple text-sm">元に戻す</span>
                  </div>
                  <div class="flex justify-between bg-medium-blue p-2 rounded">
                    <span class="text-cream">Ctrl + D</span>
                    <span class="text-light-purple text-sm">複製</span>
                  </div>
                  <div class="flex justify-between bg-medium-blue p-2 rounded">
                    <span class="text-cream">Delete</span>
                    <span class="text-light-purple text-sm">削除</span>
                  </div>
                </div>
                <div class="space-y-2">
                  <div class="flex justify-between bg-medium-blue p-2 rounded">
                    <span class="text-cream">F</span>
                    <span class="text-light-purple text-sm"
                      >選択オブジェクトにフォーカス</span
                    >
                  </div>
                  <div class="flex justify-between bg-medium-blue p-2 rounded">
                    <span class="text-cream">Space</span>
                    <span class="text-light-purple text-sm">再生/停止</span>
                  </div>
                  <div class="flex justify-between bg-medium-blue p-2 rounded">
                    <span class="text-cream">W/E/R</span>
                    <span class="text-light-purple text-sm"
                      >移動/回転/拡大縮小ツール</span
                    >
                  </div>
                  <div class="flex justify-between bg-medium-blue p-2 rounded">
                    <span class="text-cream">Ctrl + Shift + N</span>
                    <span class="text-light-purple text-sm"
                      >新しいGameObject</span
                    >
                  </div>
                </div>
              </div>
            </div>

            <div class="bg-dark-navy rounded-lg p-6">
              <h4 class="text-xl font-semibold text-light-purple mb-3">
                🔧 トラブルシューティング
              </h4>
              <div class="space-y-4">
                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">
                    🚫 オブジェクトが見えない時
                  </h5>
                  <ul
                    class="list-disc list-inside space-y-1 text-cream text-sm"
                  >
                    <li>カメラの位置を確認</li>
                    <li>オブジェクトの位置を確認（Sceneビューで見る）</li>
                    <li>Rendererコンポーネントがあるか確認</li>
                    <li>Materialが設定されているか確認</li>
                  </ul>
                </div>

                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">
                    🐛 スクリプトエラーが出る時
                  </h5>
                  <ul
                    class="list-disc list-inside space-y-1 text-cream text-sm"
                  >
                    <li>Consoleウィンドウでエラー内容を確認</li>
                    <li>スペルミスがないかチェック</li>
                    <li>セミコロン（;）が抜けてないかチェック</li>
                    <li>大文字小文字を正確に入力</li>
                  </ul>
                </div>

                <div class="bg-medium-blue p-4 rounded">
                  <h5 class="font-semibold text-cream mb-2">
                    🎵 音が鳴らない時
                  </h5>
                  <ul
                    class="list-disc list-inside space-y-1 text-cream text-sm"
                  >
                    <li>AudioSourceコンポーネントがあるか確認</li>
                    <li>AudioClipが設定されているか確認</li>
                    <li>Volume（音量）が0になってないか確認</li>
                    <li>Mute（ミュート）になってないか確認</li>
                  </ul>
                </div>
              </div>
            </div>

            <div class="bg-light-purple bg-opacity-20 p-4 rounded">
              <p class="text-cream">
                💡 <strong>猿ポイント：</strong>
                分からないことがあったら、まずはUnityの公式ドキュメントを見ましょう！
                英語が苦手なら、Google翻訳を使うのも手です。
                あとは、YouTubeの解説動画もとても参考になります！
              </p>
            </div>
          </div>
        </div>
      </section>
    </main>

    <!-- フッター -->
    <footer class="bg-medium-blue py-8">
      <div class="max-w-4xl mx-auto px-4 text-center">
        <p class="text-cream mb-2">🦍 猿でもわかるUnity取説</p>
        <p class="text-light-purple text-sm">
          頑張れば誰でもゲームが作れます！一歩ずつ進んでいきましょう！
        </p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "App",
  mounted() {
    // スムーズスクロール
    document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
      anchor.addEventListener("click", function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute("href"));
        if (target) {
          target.scrollIntoView({
            behavior: "smooth",
            block: "start",
          });
        }
      });
    });
  },
};
</script>
