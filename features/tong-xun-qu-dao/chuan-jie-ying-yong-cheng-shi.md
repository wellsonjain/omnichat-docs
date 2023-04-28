# 串接應用程式

## 串接電商平台 Shopify

串接後會將 Shopify 的會員聯絡人同步到 Omnichat 後台中，後續有登入官網會員的客人在對話插件對話時，對話頁面中就會顯示其會員資料。（功能非自動同步，需手動同步）

### 步驟一

在 Omnichat 選單中找到串接頁面：「通訊渠道  >  串接應用程式」，並點擊 Shopify 的串接按鈕

<figure><img src="../../.gitbook/assets/截圖 2023-02-15 上午10.24.56.png" alt=""><figcaption></figcaption></figure>

### 步驟二

填入 Shopify 的 商店 URL 與 API access token

API access token 取得請參考 Shopify 的[教學手冊](https://help.shopify.com/zh-TW/manual/apps/custom-apps)

{% hint style="info" %}
管理介面 API 存取範圍需要至少授權「`read_customers」`
{% endhint %}

<figure><img src="../../.gitbook/assets/截圖 2022-12-30 下午4.18.25.png" alt=""><figcaption></figcaption></figure>

### 步驟三

串接成功後，會顯示同步按鈕，點擊「立即同步」會立刻執行同步功能

點擊「稍後同步」的話，也可以隨時回來串接應用程式的功能選單再度同步

<figure><img src="../../.gitbook/assets/截圖 2023-02-15 上午10.28.54.png" alt=""><figcaption></figcaption></figure>

串接成功的話，在應用程式的右側會顯示功能選單

<figure><img src="../../.gitbook/assets/截圖 2023-01-04 上午10.21.16.png" alt=""><figcaption><p>取得串接資料後的選單畫面</p></figcaption></figure>

1. 編輯：可以更改商店 URL 或 API access token 內容
2. 資料同步：除了能再次同步聯絡人資料到最新的狀態外，也可以看到上次同步狀態的資訊
3. 解除串接：若要取得不同商店的聯絡人，可以解除串接後再次串接

### 步驟四

完成同步後，會顯示底下畫面。

{% hint style="info" %}
同步資訊中，若「新聯絡人同步數量」為 0，代表這次同步的過程中沒有新增加的聯絡人。
{% endhint %}

<figure><img src="../../.gitbook/assets/截圖 2023-02-15 上午10.29.17.png" alt=""><figcaption></figcaption></figure>

### 會員資料同步完成後畫面

若完成同步後，可以到「聯絡人及推播訊息 > 網站」的列表中，找到 Shopify 的客人資料。

<figure><img src="../../.gitbook/assets/截圖 2023-02-15 上午10.33.03.png" alt=""><figcaption></figcaption></figure>

### 注意事項

1. 若在近期有更新連絡人，但串接後沒有看到聯絡人數量更新，請嘗試解除串接後重新串接。
