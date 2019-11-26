## 參考資訊

### aframe github
https://github.com/aframevr/aframe
中文教學
https://techbrood.com/aframe


### 動畫規則
https://github.com/donmccurdy/aframe-extras/tree/master/src/loaders

### AR產生marker
https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html

### 轉SVG工具(50K以下)
https://www.onlinewebfonts.com/icon/tools

### 轉SVG工具(這個比較猛)
https://convertio.co/png-svg/

### 一個絕對沒問題的marker產生器
http://bhollis.github.io/aruco-marker/demos/angular.html

### a-entity 紀錄
1. scale掌管大小，如果一開始沒看到可能是因為本體太大或是位置偏差可先調整如scale="0.1 0.1 0.1"

### 相關備註
1. ar周圍標記為黑框可增加辨識效率(可考慮用牌墊當底，或者本身拼圖就用黑布包裝)
2. 直線辨識度高於曲線
3. 動畫的開始與結束由setAttribute/removeAttribute處理
4. AFRAME.registerComponent需要研究
5. 確認動畫骨架概念(因為目前的動畫結束後會停留在一個詭異的動作)
6. 目前對周圍網路速度是有要求的，以一個動畫1MB+標誌20KB來計算，1MB*52+(一些工具)=55M左右．也就是說每次使用都會需要這個網路資源，若換算現在普遍4G的加載速度大約就是2~3秒
7. 效率問題，快速載入網頁(只有download marker)，但是merker找到後需要時間下載模型(約1~2秒)，或是在一開啟網頁就download(marker_model)，這樣載入時間較久(約5秒)，但是marker一掃馬上出來

### marker注意事項
1. 每個marker都要有一定的差距，不然會很慘(過去以寶寶貼圖實驗，只在旁變加上數字會有誤認的問題存在)
2. 周圍建議要全黑(可以包裝成拼圖的盒子)，如非全黑是很難判定成功的
3. 同時還要考慮到轉方向的問題，因為鏡頭是有可能判定成另外一個圖形的
4. 觀眾看到的marker要比較大，實際製作的比較小(以色塊而言)

### 3D模型建議
1. 建議模型的點盡可能地少（細節減少），沒展示出來的就算平面也沒問題(比如魔術師背後完全不存在顏色都不需要這樣的概念)
2. 牌只要花色點數就好
3. 如果可能盡量300KB以下
4. 動畫可考慮拆成兩段，第一段為魔術師動畫，第二段為牌出現

