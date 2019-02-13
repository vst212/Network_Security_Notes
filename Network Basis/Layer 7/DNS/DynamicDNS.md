# Dynamic DNS
即使所尋求的 Web 服務最近切換了 IP 地址，動態 DNS 也可以幫助確保 DNS 查詢正常工作。

## What is dynamic DNS (DDNS) ?
許多 Web 屬性（如：API 或網站）在 Internet 連接上運行，其 IP 地址經常更改，如果這些屬性的運算符想要為託管資源提供特定域名，則必須在域名系統（DNS）記錄中存儲 IP 地址，這會產生問題。動態 DNS（DDNS）是一種服務，可以使用 Web 屬性的正確 IP 地址更新 DNS，即使該 IP 地址不斷更新也是如此。
例如，如果網站管理員正在運營一個域名為 www.example.com 且 IP 地址為 1.2.3.4.5.6 的小型網站，則只要其他用戶將 www.example.com 輸入其瀏覽器，DNS 就會直接進入他們到 1.2.3.4.5.6 的服務器。 如果管理員的 ISP 動態地將 IP 更改為 1.2.3.4.5.7，則動態 DNS 服務可以自動更新管理員的 DNS 記錄，以便嘗試訪問 www.example.com 的其他用戶現在將轉到正確的 IP 地址。

## Why do some IP addresses change ?
在 Internet 發展的早期，IP 地址很少發生變化，這使得域名管理變得更加簡單。但是，具有 Internet 接入的網路和家用計算機的快速增長造成了可用 IP 地址的短缺。這導致了動態主機配置協議（DHCP），它允許 ISP 動態地為其用戶分配 IP。ISP 通常會維護一個共享 IP 地址池，並在連接期間或直到達到最大時間後，根據需要將這些 IP 地址分配或 "lease"（租賃）給用戶。儘管 IPV6 的引入緩解了 IP 地址的不足，但 ISP 仍然經常使用 DHCP，因為它比提供靜態 IP 更具成本效益。

運行主要 Web 服務的大型企業要求其 ISP 為其提供不變的或 "static" IP 地址，以便它們可以使用標準 DNS 實踐進行操作。相比之下，較小的服務往往會頻繁地看到其 IP 地址被其 ISP 更改，因此它們需要動態 DNS 解決方案來保持其 DNS 記錄的最新狀態。這些較小的服務可以包括小型企業網站、個人網站、DVR 和安全攝像頭。

## How does dynamic DNS work ?
有許多公司提供具有不同功能和技術的動態 DNS 服務。啟用動態 DNS 的一種非常常見的方法**是為用戶提供在其計算機或路由器上運行的軟體**。該軟體隨時更新 ISP 提供的 IP 地址，與動態 DNS 服務提供商進行通訊，動態 DNS 提供商按照次序使用這些更改更新 DNS，提供幾乎即時更新。