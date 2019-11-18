# <center>Line 更新快速瀏覽（2019/11/14）</center> 
<p align="right">KeyWord： #LIFF #Messaging API</p>

- - -
1. `Get content`  `Upload rich menu image` `Download rich menu image` 的Domain name更改 
2. 使用者再也不能增加`LIFF apps` 至 Messaging API channels 

- - -
## <center>更動說明</center>
#### 部分Domain name 的更改
>The domain name of certain Messaging API endpoints has been changed from `api.line.me` to `api-data.line.me`. There is no maintenance associated with this.


 呼叫端點更改，從 `api.line.me` to `api-data.line.me` 

##### 改動端點
- [Get content](https://developers.line.biz/en/reference/messaging-api/#get-content)
- [Upload rich menu image](https://developers.line.biz/en/reference/messaging-api/#upload-rich-menu-image)
- [Download rich menu image](https://developers.line.biz/en/reference/messaging-api/#download-rich-menu-image)

##### 影響

>If you are using the above endpoints, please change your domain  during the transition period. We apologize for any inconvenience this may case. Thank you for your understanding.

如果有使用這些端點，請在**過渡期更改Domain**。

> Once the transition period ends, accessing an endpoint of the old domain will return a 404 status code.

過渡期結束後，訪問舊的端點將會放回`404` 狀態碼。


##### 過渡期 ：今日 - 2020/04/30
#### 使用者再也不能增加LIFF apps 至 Messaging API channels 
>LIFF v2 is scheduled to be updated with LINE Login as the core channel. Additionally, an upcoming change will prevent users from adding LIFF apps to Messaging API channels entirely. We strongly recommend users to add LIFF apps to the LINE Login channel.

LIFF v2 要以 Line Login為核心channel來更新。這個更改將會禁止用戶將LIFF應用程序加到Messaging API的通道。
**強烈建議將LIFF應用加到LINE Login channel !**

##### 預計更動時間： 2020 2月上旬

##### 影響
| channel 類型 | 影響內容                                                                    |
| ------------ | --------------------------------------------------------------------------- |
| Login        | 不影響                                                                      |
| Messaging    | **更改規格後**無法將LIFF應用加入Messaging API。規格更改期間，LIFF依然可用。 |

##### 轉移至LINE Login channel
>To continue using the LIFF app added to the Messaging API channel, re-add the LIFF app to the LINE Login channel. Once re-added, LINE Developers console will issue a new LIFF app ID. As a result, please take note of the following:
> * If you're using LIFF v2, change the LIFF app ID specified in liff.init().
> * The LIFF URL used to launch LIFF（e.g.：line://app/1234567890-AbcdEfgh）will change.

將LIFF 應用程式重新導入LINE Login channel才能繼續使用原本在Mesaaging API channel中的原程式。
重新加入後，LINE Developers控制台會發出新的LIFF應用ID。請注意這幾點。
- 如果使用的是LIFF v2，請更改指定的LIFF應用ID `liff.init()`。
- 用於啟動LIFF的 LIFF URL 將會更改 （像是 line://app/1234567890-Abcdefg）
**避免混淆 建議完成改動後刪除原應用。**
# - - -
[原文鏈接](https://developers.line.biz/en/news/2019/11/)
翻錯通知此人：An（205）