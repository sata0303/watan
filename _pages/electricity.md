---
layout: single
title: 電力使用状況（試行）
author_profile: true
---

Chart.jsを使ってみたかったので、例として電気代の推移をグラフ化してみたい。
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.1.4/Chart.min.js"></script>

<canvas id="myChart" width="400" height="400"></canvas>
<script type="text/javascript">
  // データ --- (*1)
  const data = {
    labels: ['A', 'B', 'C', 'D', 'E'],
    datasets: [{
      label: '国語のテスト',
      data: [78, 64, 35, 90, 83]
    }]}
  // グラフを描画 --- (*2)
  const ctx = document.getElementById('chart_cv')
  const chart_cv = new Chart(ctx, {
    type: 'bar', // グラフの種類
    data: data, // データ
    options: {}}) // オプション
</script>



*参考：東京大学の電力使用状況　http://ep-monitor.adm.u-tokyo.ac.jp/campus/denryoku
（2021年1月18日アクセス）