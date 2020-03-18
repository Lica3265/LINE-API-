# <center>Line Bot 小聚（2020三月初）</center> 
<p align="right"></p>

- - -
議程
1. Line Api更動
2. 口罩銷量查詢Line Bot 實戰經驗分享
3. 其他經驗分享
- - -
## <center>更動說明</center>
#### Line API更動分享
1. LIFF v1 本來三月底會停用 Server API 這件事情會取消
2. Narrowcasting and audience(精準化訊息推播)
也就是訊息分眾 
分眾如何解決問題
客戶不會討厭廣告，他們只想要他們看到的廣告
讓客戶點擊再行銷
3. 未來停用BLE功能（藍芽相關模組）
4. LIFF Share target picker 
   一種讓用戶可以送Flex message的方式


#### 口罩銷量查詢Line Bot 實戰分享
這次分享主要不是在講Line Bot如何實作
而是講解Azure的一些實用功能。

開發經驗分享
首先先思考主要功能為何？
1. 關鍵字查詢
2. 地圖座標查詢

再思考實作上困難以及技術節點 
1. 如何確保快速更版不會影響使用者體驗
解法：利用Azure提供的藍綠部署模式，可是使用者完全沒有感覺到更版帶來的影響。
![兔](https://i.imgur.com/jCUGAdZ.png)

2. 如何更新資料
解法：利用Azure的“確保網站可用”功能，每五分鐘去戳Web API。

3. 如何確保系統卡頓問題節點
解法：利用Azure 系統可用率分析（如圖為政府API出問題）找出最為緩慢的部分
![兔](https://i.imgur.com/SDde2I9.png)
# - - -

有更多消息想了解通知此人：An（分機：205）