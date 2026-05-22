# PA 廠商會議問題清單 (v0.7)

以下為針對 PA 防火牆汰換專案，提供給廠商於技術會議中討論與釐清之核心問題：

1. **HPE-5130-01 潛在迴圈風險處理**：
   - 目前已知 FortiGate LAN1 與 LAN2 分別接入 5130-01 的 port 48 與 port 12。
   - 在 5130-01 port 12/48 VLAN 模式 (access/trunk/hybrid) 皆為**待確認**的情況下，PA 防火牆在介面銜接與移轉時，應如何規劃以避免 L2 迴圈或廣播風暴？

2. **Core01 Port 16 骨幹 Tagged VLAN 對接方式**：
   - Core01 port16 目前承載 VLAN1 (untagged)、VLAN2 (tagged) 及 VLAN3 (tagged)。
   - 在 PA 遷移時，針對這些 Tagged VLAN2/3 路由與策略，PA 上應如何配置 (例如：Sub-interface 或 Trunk) 才能確保與現有核心無縫對接？

3. **無線網路 (WiFi) 分區設計**：
   - WiFi 流量目前由 Cisco 9200 (供電給下游 FortiAP) 匯聚至原 FortiGate 的 port5。
   - 針對 WiFi / Cisco 9200 / FortiAP 網段，是否建議在 PA 上切分獨立 Zone 以進行更完善的資安管控？

4. **監視器 (CCTV) 網段獨立規劃**：
   - 目前 CCTV 設備流量混入主要之 LAN1 網段。
   - PA 導入時，CCTV 是否要建立獨立的 Zone？若規劃獨立 Zone，在不更動既有下游 Edge Switch VLAN 設定的前提下，廠商是否有建議的實作手法？

5. **高密度終端與舊光纖分支測試涵蓋**：
   - 校內有兩大高密度終端分支，分別為 Core01 port12 (舊光纖至 1F 幼兒園廁所旁分機櫃，約 101 MACs) 與 Core01 port9 (接 HPE-5130-03，約 129 MACs)。
   - 這兩處網路環境應如何納入 PA 上線時的優先壓力測試與連線驗證範圍？