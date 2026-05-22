# School Network Topology v0.6 Handoff Package

## 用途說明
本資料包為校園網路架構盤點的 v0.6 版本移交檔案。主要用於呈現目前盤點出的網路拓樸現況，並作為後續 PA 防火牆汰換專案、廠商網路查修及設備管理的參考基準。

## 資料來源
本資料包之資訊整合自以下來源，並**全程採離線靜態分析**，未對現有設備執行任何侵入式掃描或設定變更：
- FortiGate CLI 設定檔與路由表
- HPE 3810M Core01 SNMP 查詢結果 (MAC table, LLDP, Port status)
- 現場設備實體接線照片與勘查紀錄

## 版本資訊
- **Version:** v0.6
- **Date:** 2026-05-22

## 內容物說明
1. `topology_summary_v0_6.md`: 校園網路拓樸之文字總結與現狀描述。
2. `topology_v0_6.mmd`: Mermaid 格式的分層網路拓樸圖 (L0-L3)。
3. `school_topology_v0_6.html`: 互動式網頁版拓樸圖，支援離線瀏覽與節點資訊查詢。
4. `pa_migration_checklist_v0_7.md`: PA 防火牆汰換前之盤點與風險確認檢查表。
5. `vendor_request_5130_readonly_v0_6.md`: 針對 HPE-5130-01 設備之唯讀權限申請與設定檔需求清單。

## 安全性聲明
- 本資料包內容僅供網路架構釐清與規劃使用。
- 盤點過程**未**產生任何修改設定指令，亦**未**執行 SNMP 密碼猜測等行為。
- 所有未確認之 IP、MAC 或 Port 狀態均已標示為「待確認」，在未釐清前**不建議**逕行修改任何設備之 VLAN 或 SNMP 設定。