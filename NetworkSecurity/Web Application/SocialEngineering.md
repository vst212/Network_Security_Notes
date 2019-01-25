# Social Engineering Attack
在 Social Engineering （社交工程）攻擊中，受害者被操縱**移交**可用於惡意目的的敏感訊息。

## What is social engineering ?
從廣義上講，社交工程是操縱人們放棄敏感訊息的做法。社交工程攻擊可以發生在人身上，例如：一個裝扮成送貨員的闖入建築物的竊賊。本文將重點關注社交工程網路攻擊。在大多數情況下，這些攻擊指在**讓受害者洩露登錄憑據或敏感的財務訊息**。

- 攻擊者向受害者發送電子郵件，該電子郵件似乎來自受害者聯繫人列表中的某人。此電子郵件可能包含可疑鏈接，該鏈接將執行惡意 `cross-site scripting` 攻擊，或將受害者指向惡意站點。
- 攻擊者使用聲稱可以下載流行電影或軟體的鏈接線上誘餌用戶，但這些下載實際上包含惡意負載。
- 攻擊者聯繫一名聲稱是富有的外國人的受害者，該外國人需要美國銀行帳戶訊息來轉移他們的財富，提供獎勵受害者以換取他們的銀行帳戶信息。實際上，攻擊者正在排除受害者的賬戶。

![](https://www.cloudflare.com/img/learning/security/threats/social-engineering-attack/social-engineering-fake-login-page.svg)

除了這些類型的小型和個人社交工程詐騙之外，還有更複雜的社交工程攻擊可以利用整個組織，例如：thumb-drive drops。這些攻擊可以針對受到良好保護的公司網路，甚至是那些沒有連接到 Internet 的公司。攻擊者透過在目標公司的停車場周圍分散幾個 USB drives 來做到這一點。他們在這些 drives 上放置了一個誘人的標籤，例如：機密，希望一些好奇的員工會找到一個並將其插入到他們的計算機中。這些 drives 可能包含非常具有破壞性的`病毒`或`蠕蟲`，因為它們是從本地計算機進入網路而難以檢測的。

## What are some famous examples of social engineering attacks ?
2011 年數據洩露 RSA 引起了巨大轟動，主要是因為 RSA 是一家值得信賴的安全公司。這一漏洞破壞了 RSA 廣受歡迎的 two-factor 身份驗證服務 SecurID。雖然攻擊的所有細節尚未公開披露，但眾所周知，它始於社交工程攻擊。這次攻擊是通過基本的 phishing （網路釣魚）攻擊發起的，攻擊者向低級 RSA 員工發送的電子郵件似乎是關於招聘的公司電子郵件。

美聯社在 2013 年成為社交工程攻擊的受害者，導致 1360 億美元的股市暴跌。 再一次，這是透過發送給員工的網路釣魚攻擊來實現的，透過簡單的打開電子郵件中的鏈接，其中一名員工觸發了攻擊，導致 AP 的 Twitter 帳戶遭到入侵，並且攻擊者在推特上發布了關於白宮爆炸的假新聞報導，這個虛假的新聞報導迅速流傳，導致道瓊工業指飆升 150 點，被稱為敘利亞電子軍的敘利亞黑客組織聲稱對此次襲擊負責，但從未提供任何證據。

由於其複雜程度，2013 年針對 Target 的數據洩露攻擊已經成為歷史上最惡名昭著的網路攻擊之一。與此處提到的其他人一樣，此攻擊始於社交工程，但攻擊者並未追蹤任何為 Target 工作的人。相反，他們向在 Target 商店安裝了高科技空調的供暖和空調供應商的員工發送了電子郵件，這些空調與 Target 的店內計算機系統相關聯，一旦攻擊者能夠破壞第三方供應商，他們就可以攻擊 Target 的網路並從數千家商店的信用卡掃描儀收集信用卡信息，公佈約 4000 萬目標客戶的財務數據。

## How to protect against social engineering attacks
雖然電子郵件篩選等自動安全功能可以幫助防止攻擊者與受害者聯繫，但是針對社交工程攻擊的最佳防禦是常識，並結合了對流行社會工程攻擊的最新知識。美國計算機應急準備小組（US-CERT）建議公民警惕任何可疑通信，並僅在安全網頁上通過網路提交敏感信息（HTTPS 和 TLS 是網站安全的良好指示）。他們還建議避免點擊電子郵件中發送的鏈接，而是直接在瀏覽器中輸入可信公司的網址。