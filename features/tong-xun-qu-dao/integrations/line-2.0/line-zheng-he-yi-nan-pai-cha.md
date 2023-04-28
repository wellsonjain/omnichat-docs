# LINE 整合疑難排查

{% hint style="info" %}
若整合 Omnichat 之後，無法正常在 Omnichat 收到 LINE 的訊息或者無法在 Omnichat 發訊息給 LINE 帳號，請依照以下的步驟檢查是否在整合 LINE 的過程有錯誤
{% endhint %}

### 1. 在 LINE 官方帳號後台檢查是否在聊天機器人模式以及 Webhook 是否開啟

&#x20;進入 LINE 官方帳號後台 --> 設定 --> 回應設定，檢查 **回應模式**是否為 **聊天機器人。**另外檢查 **Webhook** 是否是 **啟用**

<figure><img src="../../../../.gitbook/assets/Line OA後台 (2).png" alt=""><figcaption></figcaption></figure>

### 2. 檢查 Messaging API 設定是否正確

&#x20;進入 LINE 官方帳號後台 --> 設定 --> Messaging API，檢查 Messaging API 所設定的 **Channel ID** / **Channel secret** / **Webhook** 網址是否與 Omnichat 後台的[**串接社群通訊渠道**](https://app.easychat.co/integration.html)之設定相同

![](<../../../../.gitbook/assets/line integration check 3.png>)

### 3. 進入 Line Developers 後台檢查設定是否正確

由第二點所提供的圖片上有個 LINE Developers 後台入口進入開發者後台。

進入 LINE Developers 後：

1/ 點擊右上方的頭像，並選擇你的帳號 \
2/ 選擇 Provider（服務提供者）\
3/ 選擇 Channel（官方帳號）\
4/ 進入「Basic Settings」和「Messaging API 」兩個分頁

![](<../../../../.gitbook/assets/串接 line 09.jpg>)

![LINE 官方帳號 Messaging API 設定頁面](<../../../../.gitbook/assets/螢幕快照 2019-12-31 下午12.28.56.png>)

#### 檢查相關設定是否正確

&#x20;檢查 **App name** / **Channel ID** / **Channel Secret，**等內容是否與 Omnichat 後台的[**串接社群通訊渠道**](https://app.easychat.co/integration.html)之設定相同

![](<../../../../.gitbook/assets/line integration 2.0 -4 (1).png>)

![](<../../../../.gitbook/assets/line integration 2.0 -5.png>)

上述檢查完成後繼續檢查以下項目

1. **Available feature** 裡必須有 **REPLY\_MESSAGE** 跟 **PUSH\_MESSAGE** 這兩項，若少了其中一項可能是在升級 LINE 官方帳號 2.0 的過程中 LINE 那方有錯誤發生，請洽 LINE 客服。若您是用 LINE@ 帳號，則可能是你的 LINE 付費方案並沒有 Messaging API，請升級方案。
2. 檢查 **Webhook URL** 是否與 Omnichat 後台的**串接社群通訊渠道**之設定相同。
3. **Use webhook 為 開啟**
4. 檢查 **Channel access token** 是否與 Omnichat 後台的**串接社群通訊渠道**之設定相同。

![](<../../../../.gitbook/assets/螢幕快照 2019-12-31 下午12.33.31.png>)

![檢查 Channel access token 是否與 Omnichat 後台設定吻合](<../../../../.gitbook/assets/line integration 2.0 -8.png>)

### 4. 進入 Line Developers 後台更新 **channel secret** 與  **access token**

如確認Line Developers 後台資訊與Omnichat 後台的**串接社群通訊渠道**之設定相同，整合串接依然失效，請至 Line developers後台重新更新 **channel secret** 與  **access token** ，複製新的**channel secret**與**access token** 到Omnichat後台『串接社群通訊渠道』，按下『更改』重新更新

![按下『Issue』取得新的Channel Secret ](<../../../../.gitbook/assets/Screen Shot 2021-09-30 at 12.29.04 PM.png>)

![按下『Reissue』取得新的Channel Secret ](<../../../../.gitbook/assets/Screen Shot 2021-09-30 at 12.29.10 PM (1).png>)







