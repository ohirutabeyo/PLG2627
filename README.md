# PL2627 — Premier League 2026/27 Tactical Dossier

Premier League 2026/27シーズン上位17クラブの戦術ドシエ。

🌐 **Live**: https://ohirutabeyo.github.io/PLG2627/

---

## 📐 プロジェクト方針

### ベースシーズン
- **対象**: 2026/27シーズン
- **順位ベース**: 2025/26最終順位（西ハム、バーンリー、ウルブズ降格、上位17クラブが対象）
- **EAFCレーティング**: EAFC26（公式リリース版）

### 戦術の前提
- 監督交代が決定/濃厚なチームは**新監督の戦術ベース**
  - 例: チェルシーはエンソ・マレスカ→リアム・ロセニアー→**シャビ・アロンソ**（26-27就任）の戦術で構築
- 監督続投チームは現行戦術ベース
- 各チーム、**守備時 + 保持時**の2つの可変フォーメーションを図解

### 移籍動向（70%基準）
- **離脱リスク70%以上**: 図中の選手をオレンジボーダーでマーク + 代替選手名併記
- **補強候補70%以上**: 該当ポジションを緑ボーダーでマーク + 補強候補選手名併記
- 70%未満の動向は注釈エリアにメモとして記載

### 選手名表記
- すべて**カタカナ**
- **同チーム内に同名選手が複数いる場合は、必ずイニシャル/フルネーム/通称で区別**
  - ❌ Bad: 「ガブリエウ」のみ（アーセナルには3人いる）
  - ✅ Good: 「ガブリエウ（マガリャンイス, CB）」「G・ジェズース（ST）」「マルティネッリ（LW）」
- キャプテンには `(C)` を付記

---

## 🎨 デザイン仕様

### 共通レイアウト
1. **HEADER**: チーム名 + フォーメーション + 監督情報
2. **INFO STRIP**: 戦術アイデンティティ / 保持時の形 / 非保持時 / 前年成績
3. **TACTICAL BRIEFING**: 戦術概要 + 守備時図 + 保持時図 + ポジション役割解説
4. **LEGEND**: 凡例（通常/GK/離脱リスク/補強候補）
5. **NOTES**: 離脱動向 + 補強動向
6. **FOOTER**: ドシエ番号など

### カラーシステム
- 各チームのプライマリカラーをCSS変数 `--{team}` で定義
- ヘッダーグラデーション、フォーメーションバッジ、選手ディスクなどに適用
- GK = ゴールド系で統一
- 離脱リスク = オレンジ系（`#e8a04a`）
- 補強候補 = グリーン系（`#5fb88a`）

### タイポグラフィ
- 見出し: Cormorant Garamond（セリフ）
- 本文: Inter + Noto Serif JP
- 数値・コード: JetBrains Mono

---

## 📁 ファイル構成

```
PLG2627/
├── README.md           ← プロジェクト方針（このファイル）
├── HANDOFF.md          ← Claude Code向け作業指示書
├── index.html          ← 17チーム一覧トップ
├── arsenal.html        ← 1位
├── chelsea.html        ← 10位（テンプレ参考）
└── （以下、残り15チーム）
```

---

## ✅ 進捗

- [x] 01. Arsenal (`arsenal.html`)
- [x] 02. Manchester City (`mancity.html`)
- [x] 03. Manchester United (`manunited.html`)
- [x] 04. Aston Villa (`astonvilla.html`)
- [x] 05. Liverpool (`liverpool.html`)
- [x] 06. Bournemouth (`bournemouth.html`)
- [ ] 07. Sunderland
- [ ] 08. Brighton
- [ ] 09. Brentford
- [x] 10. Chelsea (`chelsea.html`)
- [ ] 11. Fulham
- [ ] 12. Newcastle United
- [ ] 13. Everton
- [ ] 14. Leeds United
- [ ] 15. Crystal Palace
- [ ] 16. Nottingham Forest
- [ ] 17. Tottenham

---

## 🛠️ Tech
- Pure HTML / CSS（フレームワークなし）
- 外部依存: Google Fonts のみ
- スマホ最適化済み（レスポンシブ）
- ホスティング: GitHub Pages
