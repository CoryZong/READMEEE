# Link8 - 圖書館系統前台建置

[TOC]



## 1.首頁 (共7小時)

### (1) 網頁架構 
#### 導航列 
:::info
* 共用組件引入 : 導航列。
:::

#### 類別Tabs (API-get) => 1小時
:::info
* ant design : Tabs。
* Flex-box : 類別Tabs(div)。
* 類別Tabs onclick : 跳頁至"分類排序頁"
:::

#### 類別輪播圖 (API-get) => 4.5小時
:::info
* ant design : Carousel 、 Button。
* Flex-box : 類別輪播圖(div)。
* 書籍Hover : 跳出書籍簡介彈窗(div)。
  * Flex-box : 愛心數&借閱數(div) 。
* 書籍中封面(第一層彈窗)onclick : 書籍資料彈窗(div)。
  * Flex-box : 書籍基本資訊(div) 、 簡介&目錄&序(div) 、 相關書籍(div) 、 書籍評價(div)。
:::

#### Footer => 0.5小時
:::info
* Flex-box : Footer(div)
:::

#### 分類搜尋頁  => 1小時
:::info
* 網頁架構
  * 導航列 : 導入共用組件。
  * 類別Tabs 
* Flex-box : 排序Icon&刪除Icon(div) 、 分類搜尋結果18筆(div)
:::


### (2) 使用者操作

#### 導航列
:::success
* Logo圖 : 點擊回到首頁。
* Input框 : 輸入內容時下方列出相關關鍵字，送出搜尋icon時搜尋所有書籍(類別名稱Tabs不顯示)。
* 我的書房、我的最愛、書籍採購單、後台超連結 : 連結至各頁面。
* 小鈴鐺Icon : 點擊顯示借還書資訊、欲採購書籍採購完畢，顯示所有新通知、近10筆舊通知。
* 頭像Icon : 點擊後可修改個人頭像圖片、預設頭像(男生、女生分別)。
:::

#### 類別Tabs
:::success
* 未點擊時預設顯示類別輪播圖，點擊時獲得分類查詢結果。
:::

#### 類別輪播圖
:::success
* 依類別分別顯示輪播圖，每行6本書，可滑動9次，共顯示54本書。
* 滑鼠移至書上方時，顯示第一層彈窗 : 書籍中封面、書籍愛心數、書籍借閱數、書籍借閱狀態。
* 第一層彈窗點擊書籍中封面後，顯示第二層彈窗 : 書籍資訊、簡介、目錄、序 & 相關書籍(關聯最高的九筆) & 書籍評價(該使用者評論置頂)。
:::

#### Footer
:::success
* 觀看借閱須知、掃描官方帳號Line QR-code。
:::

#### 分類搜尋頁

### (3) 本頁切割組件
:::info
* Footer
:::

### (4) 共用組件導入
:::info
* NavigationBar
* 書籍資料彈窗
:::



***



## 3.個人資料-我的書房 (共2小時)
### (1) 網頁架構
#### 導航列 
:::info
* 共用組件引入 : 導航列。
:::
#### 我的書房list : 篩選狀態select 、 書籍資訊 、 書籍借閱狀態 、續借/取消預約Button
:::info
* ant design : List
* 篩選狀態select : 排序購書資料list內容。
* 續借Button onclick : 是否續借彈窗。
  * 是否續借彈窗確定Button onclick : 續借成功彈窗or預約排隊成功彈窗。
* 取消預約Button onclick : 成功取消預約彈窗。
:::

### (2) 使用者操作 
### (3) 本頁切割組件 
:::info

:::
### (4) 共用組件導入
:::info
* NavigationBar
:::


***



## 4.個人資料-我的最愛 (共2小時)
### (1) 網頁架構
#### 導航列 
:::info
* 共用組件引入 : 導航列。
:::
#### 我的最愛list : 書籍資訊 、 目前排隊人數(排隊人頭像) 、 借閱狀態 、總借閱數 、 總愛心數 、 相似書籍Button 、 預約Button
:::info
* ant design : List 、  Carousel。
* 相似書籍Button onclick : 下方呈現相似書籍輪播圖(關聯較高的9筆)。
:::
### (2) 使用者操作 
### (3) 本頁切割組件 
:::info
* 相似書籍輪播圖 
  * 詳細內容Button onclick :  書籍資料彈窗。
:::
### (4) 共用組件導入
:::info
* 預約確認彈窗、預約成功彈窗。
* 出借中彈窗確認預約彈窗、排隊成功彈窗。
* 書籍資料彈窗。
:::


***



## 5.書籍採購單 (共4小時)
### (1) 網頁架構
#### 導航列 
:::info
* 共用組件引入 : 導航列。
::: 
#### Input搜索框 => 0.5小時
:::info
* ant design : input。
:::

#### 購書&組員購書申請清單Tabs  => 0.5小時
:::info
* ant design : Tabs。
:::
#### 購書清單內容 : 新增書籍Button 、 篩選狀態select 、 購書資料list  => 1小時
:::info
* ant design : Button 、 List 、 Select 、 Modal。
* 新增書籍Button onclick : 跳頁至"新增採購頁"。
* 篩選狀態select : 排序購書資料list內容。
* 購書資料list : 書名、申請日期、採購狀態、編輯/刪除按鈕。
  * 編輯按鈕onclick : 跳至"新增採購頁"。
  * 刪除按鈕onclick : 彈窗確認是否刪除。
:::
#### 組員購書申請清單內容 : 全選Button 、 審核Button 、 篩選狀態select 、編輯購書資料list => 1小時
:::info
* ant design :  Button 、 List 、 Select 、 Modal。
* 全選Button onclick : 顯示審核Button。
* 篩選狀態select : 排序購書資料list內容。
* 編輯購書資料list : 書名、申請日期、申請者、書店網址、售價。
  * 下方顯示總售價。
:::
#### 新增採購頁 => 1小時
:::info
* ant design :　Modal。
* Flex-box : 書籍基本資料輸入(div) 、 簡介&目錄&序(div) 、確認取消按鈕(div)。
  * 確認按鈕onclick : 彈窗確認是否申請。
:::


### (2) 使用者操作 
#### NavigationBar : (同首頁)
#### Input搜索框
:::success
* Input框 : 搜索書名、ISBN、作者、出版社、申請人(主管權限顯示)。
:::

#### 購書&組員購書申請清單Tabs
:::success
* 新增書籍onclick : 跳頁至新增採購頁。
:::

#### d. 篩選狀態select : 篩選採購狀態&時間排序
#### e. ....

### (3) 本頁切割組件 
:::info
:::

### (4) 共用組件導入
:::info
* NavigationBar
:::
***



## 共用組件 (共X小時)
### 導航列 => 1小時 
:::info
* ant design : input 、 Button。
* Flex-box : NavigationBar(div) 、 超連結們(div) 、 Icon們(div)。
* position : sticky置頂。
:::

### 書籍資料彈窗
### 預約確認彈窗
### 預約成功彈窗
### 出借中彈窗確認預約彈窗
### 排隊成功彈窗


