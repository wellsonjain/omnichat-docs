---
description: 此功能限有購買 WhatsApp Business API 方案用戶使用
---

# WhatsApp 對話統計

WhatsApp 的對話統計頁面會顯示免費與付費的對話數量，並以圖表呈現付費對話總數費用。而在此統計表當中的數值為<mark style="color:red;">**近似值**</mark>，實際收費請以每月所收到的 WhatsApp 對話費用明細為準。

以下針對該頁面當中會呈現的數據逐一進行說明

### 日期區間 <a href="#day" id="day"></a>

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午5.30.10.png" alt=""><figcaption></figcaption></figure>

* 一開始進到該頁面的預設日期，是從當天開始計算到過去的 14 天（兩週）
* 可點選日期，去篩選特定日期區間的數據
* 搜尋新日期區間後，整個頁面的數據會同時一起更新
* 當日數據更新頻率為：每小時/次
* 「所有地區」可篩選特定地區的聊天統計對話量，分為：全部地區、亞洲地區、非亞洲地區
* 最左側呈現有串接到 Omnichat 的 WhatsApp Business API （以下簡稱為 WABA）的電話號碼，若有串接多支電話號碼可從下拉式選單中篩選需要查看的 WABA 帳號

### 左側對話量統計說明 <a href="#leftconversationwaba" id="leftconversationwaba"></a>

<div>

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午5.33.39.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午5.33.43.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午5.33.47.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午5.33.52.png" alt=""><figcaption></figcaption></figure>

</div>

_可點擊上方圖片放大檢視_

由於 WhatsApp Business API 的對話收費方式會依照由商家端/用戶端開啟對話，以及所在地區進行計費，因此在對話統計表當中將會呈現是由哪一段開啟對話的相關資料

關於收費的方式，2023/6/1 WhatsApp 官方有針對新的計費方式公布相關做法，可先參考[此篇文件的說明](https://blog-hk.omnichat.ai/whatsapp-business-api-pricing-2023/)

* 所有對話 = 由商家發起（Business-initiated）的對話與用戶發起（User-initiated）的總訊息數，其中又細分為由商家發起 & 用戶發起的單項對話數的計算
* 免費對話 = WhatsApp Business API 針對商家端提供每個月 1,000 則的訊息數量（包含商家發起與用戶發起，此規則將於 2023/6/1 更改為僅計算由用戶發起）。
* 免費方案 = 此處將顯示您目前使用免費方案的用量，若以上圖為例，則表示當月份已經使用了 280 則的免費訊息則數。若想得知剩餘的免費訊息數量，可以 1,000 - 280 = 720 得知，當月份免費訊息則數仍有 720 則的餘額。免費方案訊息則數將會在每個月1號時重新計算。
* 免費入口點 (Free Entry Point Conversations) = 當**客人端**透過，廣告當中置入 WhatsApp 行動呼籲按鈕（Call to Action) 或是在 Facebook 粉絲專頁當中放上 WhatsApp 的行動呼籲按鈕**來與商家端進行訊息互動**，該訊息即屬於免費入口點對話，該筆對話將不會產生訊息費用。\
  <mark style="color:blue;">**＊注意事項：從免費入口點的第一次對話為免費，而之後的對話則需要收費；免費入口點對話僅能由用戶端發起。**</mark>
* 付費對話 = 包含由商家發起與用戶發起的需收費訊息統計數
* 費用 = 此處將以團隊所在地區顯示訊息費用，計算由商家發起以及用戶發起的金額總計

### 右側對話圖表統計說明 <a href="#rightconversationwaba" id="rightconversationwaba"></a>

下列圖表均可以透過**「下載 CSV」**檔案的功能匯出相關日期區間報表，可參考下圖範例

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午6.22.10.png" alt=""><figcaption><p>下載 CSV 檔案後的範例格式</p></figcaption></figure>

檔案中欄位包含：日期、WABA 帳號號碼、所在地區、國碼、發起對話方、訊息類型（免費/付費）、訊息數量、費用等欄位可進行查看

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午5.23.58.png" alt=""><figcaption><p>WABA 所有對話統計表</p></figcaption></figure>

* 全部：包含商家發起的對話數量與用戶發起對話數量總計（藍色線）
* 商家發起：為由商家端發起的對話數量（綠色線）
* 用戶發起：為由用戶端發起的對話數量（橘色線）

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午5.24.02.png" alt=""><figcaption><p>WABA 免費對話統計表</p></figcaption></figure>

* 全部：為免費方案與免費入口點的訊息數量總計（藍色線）
* 免費方案：為 WhatsApp Business API 每個月 1,000 則免費訊息數量使用狀況總計（綠色線）
* 免費入口點：為用戶端透過廣告上的行動呼籲按鈕（ Call to Action）或 Facebook 粉絲專頁中的 WhatsApp 行動呼籲按鈕傳送的訊息數量總計（橘色線）

<figure><img src="../../.gitbook/assets/截圖 2023-03-13 下午5.24.11 (1).png" alt=""><figcaption><p>付費對話統計與費用表</p></figcaption></figure>

* 付費對話：包含由商家發起與用戶發起的<mark style="color:blue;">**訊息數量總計**</mark>（藍色線）
* 商家發起對話：為商家發起的<mark style="color:blue;">**訊息數量總計**</mark>（綠色線）
* 用戶發起對話：由用戶發起的<mark style="color:blue;">**訊息數量總計**</mark>（橘色線）
* 費用：以商家端所在地區呈現幣值，顯示包含商家發起對話與用戶發起對話的<mark style="color:orange;">**總訊息費用**</mark>（粉色線）
* 商家發起費用：為商家發起的<mark style="color:orange;">**訊息費用總計**</mark>（淺灰色線）
* 用戶發起費用：為用戶發起的<mark style="color:orange;">**訊息費用總計**</mark>（深灰色線）
