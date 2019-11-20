# <center>Line 更新快速瀏覽（2019十月份）</center> 
<p align="right">KeyWord： #LIFF #Messaging API #Social API #LINE Login  #LINE SDK</p>

- - -
1. 新增用於好友統計的Messaging API
2. LIFF v2發佈
3. 新的ID驗證端點（verification endpoint）

- - -
## <center>更動說明</center>
#### 1.新增用於好友統計的Messaging API


**LIFF v1將被棄用**

##### 使用LIFF v2應用現在可以在外部瀏覽器中運行
這意味著可以用一般Web APP的開發環境來開發LIFF應用程序，v1版本無法使用這個功能。

##### 獲取用戶個人資料和電子郵件
由於與LINE Login v2.1的兼容性已改進，因此可以從LINE平台檢索用戶的ID和電子郵件地址。LIFF應用程序可以使用這些數據來提供與用戶信息和發送電子郵件相關的功能。

此外，即使LIFF應用程序在外部瀏覽器中運行，您也可以使用LINE Login（網絡登錄流程）。這意味著即使LIFF應用程序在外部瀏覽器中運行，您也可以使用相同的信息。

##### 讀取QR碼
可以啟動LINE的QR碼閱讀器並獲取用戶讀取的字符串。

##### 獲取LIFF應用環境信息
可以獲得有關LIFF應用程序運行環境的以下詳細信息：

* 運行LIFF應用程序的操作系統（iOS，Android，外部瀏覽器）
* LIFF應用程序是否正在應用程序內瀏覽器中運行（true,false）
* 語言設定
更多信息，請參見[LINE前端框架](https://developers.line.biz/en/docs/liff/overview/)。

#### 3.新的ID驗證

以前後端伺服器收到來自 LINE Login v2.1 或 LINE SDK 的ID token時，您應該自己驗證此token是正確的，可能是利用[JWT庫](https://jwt.io/#libraries-io)或是編寫自己的解碼和驗證代碼。

在此發行以後，只需講HTTP請求發送到驗證端點（verification endpoint）即可確定ID token是否正確。

想了解更多，請閱讀 [將 ID token 傳送到後端伺服器](https://developers.line.biz/en/docs/line-login/native/take-over-session/#transfer-id-token)

# - - -
[原文鏈接](https://developers.line.biz/en/news/2019/10/)
翻錯通知此人：An（205）