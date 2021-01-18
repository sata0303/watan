---
layout: single
title: 電力使用状況（試行）
author_profile: true
---

Chart.jsを使ってみたかったので、例として電気代の推移をグラフ化してみたい。
ちなみに、2015年に国際連合で採択された「持続可能な開発目標（Sustainable Development Goals）」の7番目のゴールとして「エネルギーをみんなにそしてクリーンに」、13番目のゴールとして「気候変動に具体的な対策を」を掲げている。

</script>
<!-- 描画先 -->
<canvas id="chart_cv"></canvas>
<!-- データを与える -->
<script type="text/javascript">
  // データ
  const data = {
    labels: ['A', 'B', 'C', 'D', 'E'],
    datasets: [{
      label: '国語のテスト',
      data: [78, 64, 35, 90, 83],
      backgroundColor: 'rgba(255,100,100, 0.5)'
    }, {
      label: '社会のテスト',
      data: [80, 52, 29, 80, 93],
      backgroundColor: 'rgba(100,100,2550, 0.5)'
    }]}
  // グラフを描画
  const ctx = document.getElementById('chart_cv')
  const chart_cv = new Chart(ctx, {
    type: 'bar',
    data: data,
    options: {}})
</script>



*参考：東京大学の電力使用状況
http://ep-monitor.adm.u-tokyo.ac.jp/campus/denryoku
（2021年1月18日アクセス）