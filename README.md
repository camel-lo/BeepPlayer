# 簡易電子琴

## 專案簡介
這是一個使用 C# Windows Forms 打造的虛擬電子琴，為「視窗程式設計 (II)」的課堂練習。與一般播放現成音效檔不同，此專案透過呼叫 Windows 系統底層 API ，直接驅動電腦喇叭發出特定頻率的聲音。

## 功能特色
* **音階發聲**：介面提供 8 個琴鍵按鈕，分別對應頻率 523Hz 到 1046Hz，點擊即可發出 300 毫秒的琴音。
* **事件共用**：8 個按鈕共用同一個 Click 事件 (`btn1_Click`)，透過讀取按鈕的 `TabIndex` 屬性來決定陣列中對應的發聲頻率，讓程式碼更精簡。
* **動態縮放介面**：實作了 `SizeChanged` 事件。當使用者拖曳改變視窗大小時，內部的琴鍵按鈕會根據初始長寬比自動按比例縮放。
<img width="422" height="123" alt="image" src="https://github.com/user-attachments/assets/018da192-e9b7-45cb-92b5-e8c315a6d918" />
<br>
<img width="429" height="375" alt="image" src="https://github.com/user-attachments/assets/9fda23aa-31f2-4a5f-be05-bda2e7f9c68a" />
