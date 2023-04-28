---
description: 透過設定並取得 LIFF ID，讓消費者不需輸入六位數驗證碼，進入 LINE 官方帳號就能完成綁定
---

# 社群身份綁定—LIFF 設定

<figure><img src="../../../../.gitbook/assets/截圖 2022-09-01 下午7.47.34.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/截圖 2022-09-01 下午7.50.46 (1).png" alt=""><figcaption></figcaption></figure>

取得 LIFF ID 需要進到 LINE Developer 後台內的 Login Channel 進行設定。如何進到 LINE Developer 後台以及 Login Channel 內注意事項，請回到[設定 LIFF ID ](she-ding-liff-id-xian-she-ding-login-channel.md#she-ding-login-channel-qian-xian-que-ren-shi-fou-yi-jing-you-line-guan-fang-zhang-hao-xiang-dui-ying)這邊的步驟

{% hint style="danger" %}
1. **綁定 LIFF ID 與遊戲模組 LIFF ID 不能使用同一個**
2. **設定後會改走 LIFF 的綁定流程（只需掃 QR CODE）**
3. **設定完畢後社群身份綁定成功訊息以『Push API』發送，LINE 方會收推播訊息費用**
{% endhint %}

順利進到 Login Channel 後，點擊「LIFF」，並按下「Add」

![](<../../../../.gitbook/assets/截圖 2022-03-31 下午4.16.13.png>)

{% hint style="success" %}
若您原本已經創建過 LIFF，可以直接點擊「Add」再新增一個 LIFF 哦
{% endhint %}

![](<../../../../.gitbook/assets/截圖 2022-03-31 下午4.15.20.png>)

#### 步驟一：將 LIFF 內部資訊填寫完畢並新增

![](<../../../../.gitbook/assets/截圖 2022-03-31 下午5.42.08.png>)

1. LIFF App name：可填寫社群身份綁定
2. Size：選擇 Compact
3. Endpoint URL：[https://app.omnichat.ai](https://app.omnichat.ai)
4. Scopes：勾選 profile、openid 和打開「view all」將內部 「chat\_message\_write」也勾選
5. Bot link feature：點選 On（Aggressive）
6. 將 Scan QR 打開
7. 按下「Add」

#### 步驟二：點擊進入剛剛創建好的 LIFF

![](<../../../../.gitbook/assets/截圖 2022-03-31 下午6.32.00.png>)

#### 步驟三：將 Endpoint URL 改成 https://app.omnichat.ai/liff-bind.html?liffId={liffId} ，並按下 Update

大括號裡面帶 LIFF ID，例如: https://app.omnichat.ai/liff-bind.html?liffId=_**1656451635-z3yqZNO3**_

![](<../../../../.gitbook/assets/截圖 2022-03-31 下午6.36.01.png>)

#### 步驟四：回到 Omnichat 後台，進到「串接社群渠道」內的 LINE，點擊「編輯」後將 LIFF ID 填入並按下「儲存」

<figure><img src="../../../../.gitbook/assets/截圖 2022-09-01 下午7.50.46.png" alt=""><figcaption></figcaption></figure>

#### 完成！當客人點擊官網上的「社群身份綁定」按鈕時，即可進到 LINE 官方帳號完成綁定！

![](<../../../../.gitbook/assets/截圖 2022-03-31 下午6.56.44.png>)
