---
layout: single
title: 電力使用状況（試行）
author_profile: true
---

Chart.jsを使ってみたかったので、例として電気代の推移をグラフ化してみたい。
ちなみに、2015年に国際連合で採択された「持続可能な開発目標（Sustainable Development Goals）」は7番目のゴールとして「エネルギーをみんなにそしてクリーンに」、13番目のゴールとして「気候変動に具体的な対策を」を掲げている。


var ctx = document.getElementById('chartjs').getContext('2d');
var monthsPriceChart = new Chart(ctx, {
    type: 'line',
    data: {
        labels: ['1月', '2月', '3月', '4月', '5月', '6月', '7月', '8月', '9月', '10月', '11月', '12月'],
        datasets: [{
            label: '取得ポイント',
            data: [13000, 11000, 14900, 8000, 19000, 12000, 10000, 18000, 11000, 13000, 14900, 18000],
            borderColor: 'rgba(54, 162, 235, 1)',
            backgroundColor: 'rgba(54, 162, 235, 0.05)',
            borderWidth: 1
        }]
    },
    options: {
        title: {
            display: true,
            fontColor: '#334d6e',
            fontSize: '20',
            text: '2019年',
        }
    }
});


*参考：東京大学の電力使用状況
http://ep-monitor.adm.u-tokyo.ac.jp/campus/denryoku
（2021年1月18日アクセス）