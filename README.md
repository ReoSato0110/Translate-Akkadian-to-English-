## 目的
- Kaggle Deep Past Challengeでのメダル獲得
- 再現可能なDeep Learningパイプラインの構築

## アプローチ概要
- ベースラインとして〇〇モデルを採用
- 前処理 → 学習 → 評価 → 推論を一貫したコードで管理
- 再現性を最優先

## 学び・仮説
- 評価指標のBLEUは、「どれだけ“連続した単語の塊”が一致しているか」。*意味は見ない
  - 語順
  - 機能語（a / the / of / to / is / was など）
  - 定型フレーズ
  - 表記の癖（記号・長音・特殊文字）
- 短い文ズル対策：Brevity Penalty
  　　短ければ一致率が高くなる逃げを防ぐ。

-ベースライン構築
  - Model: mBART / NLLB
  - Metric: BLEU

#### Next Questions
- トークナイズ（前処理で最小単位化）でBLEUはどれだけ変わる？
