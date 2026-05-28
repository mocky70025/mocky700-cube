# browserstory

Webブラウザ完結型の脱出ゲームシリーズを制作するためのプロジェクトフォルダ。

## コンセプト

PCブラウザ（主にChrome）で完結する、代名詞的作品群となる脱出ゲームシリーズを作る。
インストール不要・URLひとつで遊べる体験を前提に、ブラウザという媒体そのものを「謎」や「ギミック」に取り込むことを最大の武器とする。

## 方針

- 他媒体（ネイティブアプリ・コンソール等）では再現できない、**ブラウザならではの体験**を中心に据える
- 1作完結ではなく、複数作品で世界観・作家性を積み上げる**シリーズ前提**の設計
- ストーリー・演出・謎解きの三本柱を、ブラウザAPIの特性と噛み合わせる

## ブラウザならではのギミック候補

PCブラウザ独自の「他媒体では無理」な武器：

- 複数ウィンドウ連携（ウィンドウ間でメッセージ・座標を渡す）
- URL自体が謎（クエリパラメータ・ハッシュ・パス構造）
- DevTools 活用（コンソール・要素検査が攻略手段）
- 印刷CSS による「印刷したときだけ見える」謎
- WebAuthn（指紋・顔認証を物語に組み込む）
- WebMIDI / WebUSB / WebBluetooth 連動（外部デバイス）
- EyeDropper API（画面の色を拾う）
- カスタムURLスキーム（例: `mocky://`）
- PWA インストールで真エンディング解放
- Service Worker でオフライン化された別世界
- File System Access API による「PCのファイルに干渉する」演出
- Notifications で時間差イベント
- Web Speech API で音声入力が鍵
- カメラ・マイク（getUserMedia）を使った現実連動
- BroadcastChannel でタブ間共鳴
- History API による「戻る／進む」自体がトリック

## 利用可能なブラウザ機能カテゴリ（19分類）

調査済み。詳細はメモリ参照（claude-mem: S186-S188）。

1. 描画・ビジュアル（CSS Transform/Animation/Filter/Canvas/SVG/WebGL/WebGPU）
2. 入力（マウス/キーボード/Gamepad/WebMIDI/WebHID）
3. 音（Web Audio API/マイク/音声認識・合成）
4. 映像・カメラ（getUserMedia/MediaRecorder/Shape Detection）
5. ウィンドウ・画面（Window Management/Fullscreen/Pointer Lock）
6. ストレージ・ファイル（localStorage/IndexedDB/File System Access）
7. 通信（WebSocket/WebRTC/BroadcastChannel）
8. OS連携・ハードウェア（Notifications/WebBluetooth/WebUSB/WebAuthn）
9. メタ・URL・履歴（History API/URL params）
10. 並列・高速処理（Web Worker/SharedArrayBuffer/WebAssembly）
11. 暗号・認証（Web Crypto API/WebAuthn）
12. 機械学習・AI（WebNN/TensorFlow.js/MediaPipe）
13. VR/AR（WebXR）
14. 時間・パフォーマンス（Date/requestAnimationFrame）
15. PWA（Manifest/Service Worker/Badging/File Handling）
16. 開発者ツール・メタ遊び（console装飾/Ctrl+U/Ctrl+F/印刷CSS）
17. その他細かい機能（TextEncoder/Streams/MutationObserver）
18. CSS・HTML特殊機能（details/dialog/contenteditable/疑似要素）
19. PCブラウザ独自の「他媒体では無理」なギミック

## 次のステップ

1. 核となるギミックを 2〜3 個選定
2. シリーズ 1 作目のコンセプト（テーマ・舞台・主人公・所要時間）を決める
3. プロトタイプ着手
