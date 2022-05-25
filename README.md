# 專題題目：節奏遊戲
```
組員姓名學號：
        葉徽鄅(U10916019)  劉莉庭(U10916001)
        陳冠廷(U10916040)  吳柏毅(U10916033)
        周冠穎(U10716050)  周哲豪(U10716051)
```
##  <0>  目前進度
- [x] 需求分析
- [x] 數位設計
- [ ] 電路設計
- [ ] 編譯測試
- [ ] 結果測試
- [ ] 功能測試
- [ ] 最終結果
- [ ] 繳交
##  <1>  摘要
###     ___藉由控制紅黃綠LED燈的閃爍快慢進行節奏測試___，LED燈輪流閃爍
### 若碰到綠燈則會加一分，紅燈減一分，黃燈不加分不減分，
### 每加一分則會加快LED燈的閃爍頻率加深關卡難度，
### 得到最高分10分就會結束遊戲。
##  <2>  製作目的
###     用Quartus_II和CPLD邏輯設計實驗平台實現一個節奏遊戲，將得分在7段顯示器上顯示。
##  <3>  方法探討
###     要節奏遊戲就需要有節奏的東西，像是手機遊戲的音樂遊戲，___玩家要跟著節奏在正確的時間點按下螢幕___。
### 然而只憑這個CPLD邏輯設計實驗平台的左半邊應該是辦不到這麼複雜的設計的，
### 畢竟只能用7段顯示器、紅黃綠燈，蜂鳴器等等東西來輸出。
### 所以葉徽鄅想到，有人做過類似音樂遊戲的節奏遊戲，在正確的時間點按下按鈕即勝利。
### 於是我們想到，可以用紅黃綠燈或7段顯示器輪流閃，來做出題的動作
### 後來還討論到，可以做不同的難度(頻率越來越快)，並且可以計算得分，顯示在七段顯示器上。
### 如此一來，就要用紅黃綠燈來做出題了。
##  <4>  提出方法及步驟
###      ___選一個按鍵當作輸入，按下去後紅黃綠燈會自動有規律地輪流閃爍。
### 而若在綠燈時鬆開輸入的那個按鍵加一分；紅燈時鬆開按鍵扣一分；黃燈時鬆開按鍵則不加分也不扣分___。
### 如果做得出來，可以做不同難度的關卡(燈閃爍的頻率越來越快)。
### 為了方便按下隨時放開，我們選用 ___脈波按鍵(PULSE)___ ![image](https://github.com/sapt36/Final-project-of-DigitalCircuitExperiment/blob/main/png/%E5%9C%961.png) 來做輸入。
### 基本上只會用到一個，也就是左上角PS1按鈕。
### 需要像先前作業中那樣，在電路中加上除顫器和Clock。而要輪流跑的紅黃綠燈輪流閃
### ![image](https://github.com/sapt36/Final-project-of-DigitalCircuitExperiment/blob/main/png/%E5%9C%962.png)
### ，並且設成不同難度，最簡單的可能可以每秒換一個燈，越難頻率越快，最難的可能可以1/8秒就換一個燈。
### 而在紅燈時鬆手扣一分，黃燈時鬆手不加分不扣分，綠燈時鬆手加一分。得分則會顯示在七段顯示器上 
### ![image](https://github.com/sapt36/Final-project-of-DigitalCircuitExperiment/blob/main/png/%E5%9C%963.jpg) 
### 一開始是零分，分數隨著正確選到綠燈加上去。
### ___如果做得到的話，可以做出不同的難度，分數越高越難，也就是越快。
### 並且設一個最高分___，例如拿到十分，就會結束這個遊戲並顯示666666或是用蜂鳴器播放勝利的音樂。
##  <5>  預期成果
###     能成功讓LED輪流閃爍，且隨著關卡上升閃爍頻率也愈來越快，以實現節奏快慢的小遊戲。
##  <6>  參考文獻:point_right:
### |1|  `[CPLD邏輯設計實驗平台使用手冊]`  |  [CPLD邏輯設計實驗平台使用手冊](https://eeclass.utaipei.edu.tw/media/doc/86181)  |
### |2|  `[電路防彈跳symbol 與 clock symbol]`  |  [電路防彈跳symbol 與 clock symbol](https://eeclass.utaipei.edu.tw/media/doc/85906)  |
### |3|  `[FLIPFLOP和計數器]`  |  [FLIPFLOP和計數器](https://eeclass.utaipei.edu.tw/media/doc/88524)  |
[回到頂部](#readme)
