## 參考資訊

### aframe github
https://github.com/aframevr/aframe

### 動畫規則
https://github.com/donmccurdy/aframe-extras/tree/master/src/loaders

### AR產生marker
https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html

### 轉SVG工具(50K以下)
https://www.onlinewebfonts.com/icon/tools

### 轉SVG工具(這個比較猛)
https://convertio.co/png-svg/

### a-entity 紀錄
1. scale掌管大小，如果一開始沒看到可能是因為本體太大或是位置偏差可先調整如scale="0.1 0.1 0.1"

### 相關備註
1. ar周圍標記為黑框可增加辨識效率
2. 直線辨識度高於曲線
3. 動畫的開始與結束由setAttribute/removeAttribute處理
4. AFRAME.registerComponent需要研究
5. 確認動畫骨架概念(因為目前的動畫結束後會停留在一個詭異的動作)

### marker注意事項
1. 每個marker都要有一定的差距，不然會很慘(過去以寶寶貼圖實驗，只在旁變加上數字會有誤認的問題存在)
2. 周圍建議要全黑(可以包裝成拼圖的盒子)，如非全黑是很難判定成功的