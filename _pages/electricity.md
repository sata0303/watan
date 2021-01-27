---
layout: single
title: 電力使用状況（試行）
author_profile: false
---

Chart.jsを使ってみたかったので、例として電気代の推移をグラフ化してみたい。<br> 
ちなみに、2015年に国際連合で採択された「持続可能な開発目標（Sustainable Development Goals、いわゆるSDGs）」は7番目のゴールとして「エネルギーをみんなにそしてクリーンに」、13番目のゴールとして「気候変動に具体的な対策を」を掲げている。一人暮らしとはいえ、見える化を進めるのは節約の意味でも意義があると考える。


<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.2/Chart.min.js"></script>

<style>
#ex_chart {max-width:640px;max-height:480px;}
</style>

<canvas id="ex_chart"></canvas>

<script>
var ctx = document.getElementById('ex_chart');

var data = {
    labels: ["11月", "12月", "1月", "2月", "3月"],
    datasets: [{
        label: '電気料金',
       data: [2465, 1731, 1808, 2339, 2000],
        borderColor: 'rgba(255, 100, 100, 1)',
        lineTension: 0,
        fill: false,
        borderWidth: 3
    }]
};

var options = {
    scales: {
        yAxes: [{
            ticks: {
                min: 1200,
                userCallback: function(tick) {
                    return tick.toString() + '円';
                }
            }
        }]
    },
    title: {
        display: true,
        text: '電気料金'
    }
};

var ex_chart = new Chart(ctx, {
    type: 'line',
    data: data,
    options: options
});
</script>

<br><br>
*参考
<a href="http://ep-monitor.adm.u-tokyo.ac.jp/campus/denryoku">東京大学の電力使用状況</a><br> 
（2021年1月18日アクセス）<br>
*余裕があればガス代もそのうち。