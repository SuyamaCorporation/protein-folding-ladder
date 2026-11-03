# 30 - タンパク質折りたたみ梯子

## 概要
アミノ酸配列をアルファベット入力すると疎水性インデックスを棒グラフで表示し、HPモデルによる簡略2D折り畳み経路を可視化する教育ツール。

## 機能
- 1文字コードでアミノ酸配列入力（最大40残基）
- 各アミノ酸の疎水性インデックス（Kyte-Doolittle尺度）をSVG棒グラフで表示
- 疎水性残基（H: スコア>0, 橙色）と親水性残基（P: スコア≤0, 青色）に分類
- Canvas上に貪欲法螺旋状HPモデルの2D折りたたみ経路を描画
- HH接触（疎水性コア形成）を橙色点線で表示
- サンプル配列3種（MVLSPADKTNV・HPHPPHHPHPH・HSQGTFTSDYS）
- 20種アミノ酸のKyte-Doolittle疎水性スコア一覧表
- localStorage で最後の配列を記憶

## 技術仕様
- 静的SPA / Tailwind CDN
- SVG手描画グラフ + Canvas 2D API
- 貪欲法螺旋状格子折りたたみアルゴリズム
- escapeHtml() による XSS ガード
- aria-label / tabindex による a11y 対応
