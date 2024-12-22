# 1131-final-project-maze
Authors: 112321064 112321070
## 迷宮探索：絕地大冒險
### Input/Output unit:
* 8x8 LED 矩陣 :
透過 RGB 三色顯示不同內容：
玩家位置顯示紅色。
牆壁顯示藍色。
出口顯示綠色。
通路不發光。
遊戲結束時，所有LED8x8 矩陣顯示器閃爍。

* 七段顯示器 :
用於顯示當前關卡數字（1、2、3...）。在遊戲結束時，七段顯示器保留最後的關卡數字。

* LED 陣列 :
8 顆 LED，正常遊戲時為全關閉狀態。遊戲結束時，所有 LED 全亮。
  ![Uploading image.png…]()

* 蜂鳴器 (BUZZER)：
當玩家完成所有關卡時觸發蜂鳴器發聲，提示遊戲結束。
![image](https://github.com/user-attachments/assets/e5b740bb-38a9-4152-a0f1-666b8a40c760)

### 功能說明
* 玩家控制：
透過 UP, DOWN, LEFT, RIGHT 四個輸入按鍵，控制玩家在迷宮中的移動。
移動時檢查是否撞牆，若無阻礙則更新玩家位置。

* 遊戲地圖：
提供三個迷宮地圖，使用 8x8 的二進制陣列定義：
1 代表牆壁，玩家無法通過。
0 代表通路，玩家可以行走。
每個地圖的左下角為出口。

* 過關邏輯：
當玩家到達出口後，自動切換到下一個迷宮地圖。
若完成最後一個地圖，遊戲結束並觸發以下效果：
所有 LED 全亮。

* 蜂鳴器 (BUZZER) 發聲。
顯示器進入閃爍模式。

### 程式模組說明:
* DATA_R, DATA_G, DATA_B : 
接到 8x8 RGB 矩陣 LED 的紅、綠、藍顏色控制腳。
控制每個點的 RGB 顏色顯示（紅色=玩家，藍色=牆壁，綠色=出口）。

* COMM : 
接到 RGB 矩陣 LED 的掃描行控制腳。
控制當前被掃描的行，逐行刷新顯示器。

* SEG : 接到 7 段顯示器（Seven-Segment Display）。
顯示當前關卡數字（1, 2, 3）。

* LED : 接到 8 顆 LED 指示燈。
遊戲結束時，所有 LED 全亮；遊戲進行中，LED 全關閉。

* BUZZER : 接到蜂鳴器。
遊戲結束時，蜂鳴器響起提示玩家。
### 影片
https://drive.google.com/drive/folders/1-tzRw5pFJM_YKahRFnB8r6rL0asePRd3?usp=sharing
