# PA 防火牆介面對應表 (v0.7)

| 現有介面 / 邏輯網段 | 現有設備 (FortiGate / Core) | PA 防火牆未來介面 / Zone | 說明與狀態 |
| :--- | :--- | :--- | :--- |
| **TANet / WAN** | FortiGate WAN | 待確認 | 對外學術網路連線出口 |
| **LAN1** | FortiGate port1 (接 5130 port48) | 待確認 | 內部主要網段，目前混入監視器 (CCTV) 流量 |
| **LAN2** | FortiGate port3 (接 5130 port12) | 待確認 | 內部次要網段 |
| **WiFi / AP** | FortiGate port5 (接 Cisco 9200) | 待確認 | 無線網路服務專用網段 |
| **VLAN1** | Core01 port16 (untagged) | 待確認 | 主要設備管理與預設基礎網段 |
| **VLAN2** | Core01 port16 (tagged) | 待確認 | 待進一步確認其實際用途與對應路由 |
| **VLAN3** | Core01 port16 (tagged), 192.168.3.71/24 | 待確認 | 特定內部網段 |
| **CCTV / 監視器風險** | 現混入 LAN1 中 | 待確認 (建議評估切分獨立 Zone) | 總務處已另案通知，須確認是否納入 PA 上線時的 Zone 切分 |