---
description: 利用 CSS 調整插件位置
---

# 自行調整網站對話插件位置

## 在 Omnichat 對話插件代碼後面加上調整位置的程式碼

在 Omnichat 安裝代碼中的 `</script>` 後面 **加上** 以下代碼 (二選一，依照您的對話插件位置左右去選擇):

#### 若您的對話插件設定在右邊請加入以下代碼:

```markup
<style type="text/css">
  #easychat-floating-button {
    bottom: 15px;
    right: 15x;
  }
</style>
```

* `bottom` 後面的數字 `15px` 代表對話插件與 **網頁的最底邊界** 的距離 (預設是 15px)，若您想要讓您的插件出現在比較上面一點，請改成比 `15` 更大的數字，實際需要多大的數字可以根據您的網站 UI 配置。
* `right` 後面的數字 `15px` 代表對話插件與 **網頁的最右邊界** 的距離 (預設是 15px)，若您想要讓您的插件出現在比較左邊一點，請改成比 `15` 更大的數字，實際需要多大的數字可以根據您的網站 UI 配置。

#### 若您的對話插件設定在左邊請加入以下代碼:

```markup
<style type="text/css">
  #easychat-floating-button-left {
    bottom: 15px;
    left: 15x;
  }
</style>
```

* `bottom` 後面的數字 `15px` 代表對話插件與 **網頁的最底邊界** 的距離 (預設是 15px)，若您想要讓您的插件出現在比較上面一點，請改成比 `15` 更大的數字，實際需要多大的數字可以根據您的網站 UI 配置。
* `left` 後面的數字 `15px` 代表對話插件與 **網頁的最左邊界** 的距離 (預設是 15px)，若您想要讓您的插件出現在比較右邊一點，請改成比 `15` 更大的數字，實際需要多大的數字可以根據您的網站 UI 配置。

{% hint style="info" %}
bottom / right / left，並不需要全部都設定，若您只需要調整與下方邊界的距離，則 `left: 15px` 或者是 `right: 15px` 就不需要設定，可以整行刪除，就會維持預設的距離。
{% endhint %}

![利用 GTM 調整對話插件位置](<../../../.gitbook/assets/截圖 2021-05-03 下午12.51.19.png>)

## 範例

若設定的代碼為：

```markup
<style type="text/css">
  #easychat-floating-button {
    bottom: 50px;
    right: 50x;
  }
</style>
```

則對話插件距離 **右邊邊界** 會變成 `50px` ，距離 **下方邊界** 也會變成 `50px` 。

![](<../../../.gitbook/assets/截圖 2021-05-03 下午1.19.50.png>)

&#x20;
