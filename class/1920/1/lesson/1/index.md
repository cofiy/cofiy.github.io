[首頁] > [中華傳道會李賢堯紀念中學]

# 1. 物聯網與ObjectBlocks - 簡介

## [甚麼是物聯網（IoT）？]

相信大家都有聽說過內聯網、互聯網，那麼物聯網又有沒有聽說過呢？
在了解物聯網之前，先讓我們看看內聯網和互聯網的定義。

- 內聯網： 用於局部地區的電腦溝通網絡
- 互聯網： 用於全世界的電腦溝通網絡

![IoT]

以上兩個網絡都只用於電腦之間的溝通，而對於現時急速發展的科技社會，顯然是不夠的。於是人們在想，如何令到不是電腦的物件都可以進行數據間的溝通呢？

透過物聯網，**物件之間就可以相互溝通**。物聯網本質上也是互聯網，只是把網絡加裝與物件上面。

那麼，下一個問題就出現了。

## [物聯網可以做什麼？]

舉一個簡單的例子。

智慧燈柱可以測量當前溫度以及檢測道路狀況，**記錄數據**，並定時**回傳數據**到數據中心。數據中心就可以好好利用這些資料。例如將資料轉換為我們看得懂的資料，並以各種方式把資訊發送給我們。又或者發送給交通路燈，設定一個更適合的信號組合。

這只是其中一個非常簡單的例子，要組成智慧城市，必然有更多的組件需要去拼砌，而這也代表了**更大的難度**。

另外更小型的例子就是智能家居，大家可以想想智能家居可以怎麼實現。

![SmartCity]

## [認識Arduino]

Arduino是一個開元的微控制器版，他可以根據程式從指定界面讀取數據，並透過輸出界面控制不同的裝置。

這就像是組成**智慧城市的心臟**。大家想一想，他的工作原理像不像以上提到的例子？

![Arduino]

Arduino可以帶來很多樂趣。我們可以從最簡單的按鍵令LED燈亮，然後用他來調節燈亮程度，檢測聲音，光源。技術成熟時，還可以自己動手複雜的專題。例如可以組裝小型車、組裝抓臂、組裝攝影飛機的核心，或是自己組成小型的智能家居。

## 我的第一個ObjectBlocks專題

### ObjectBlocks是什麼？

ObjectBlocks由兩個部分組成：

- Shield Prime: 安裝Bluetooth及Wifi功能的Arduino
- ObjectBlocks.cc: 提供程式編譯器及數據面板

### 起步

在這一步，我們需要告訴程式聽，有一塊板將會成為我們的項目。只要跟著以下步驟做就可以啦。

1. 進入<https://www.objectblocks.cc>，按下Sign In，並使用**Google賬號登入**。

2. 進入Setting面板，點擊**Shield Prime**，進行Shield Prime註冊。

3. 點擊New Shield Prime，在**Shield Key**一欄輸入在Shield Prime機身上的**8位英文字串**，以及在**Name**一欄起一個你喜歡的名字（例如"My Shield Prime"）。

4. 按下**Submit**按鈕後，需要在Shield Prime機身按下**Reset**按鈕。

5. 在Shield Prime上按下Refresh按鈕後，Shield Prime便成功註冊在你的賬號上並出現在頁面列表上啦。

### 編寫程式

把板納入我們的項目之後，我們就可以開始撰寫程序啦。

1. 點擊右上角**New Project**創建新項目，在Project名稱起一個你喜歡的名字（例如"Blink"）。

2. 在側選單上，選擇**Add New Program**，在Program名稱上輸入你喜歡的名字（例如"Blink"）。

3. 你已經進入了撰寫程序的界面了。

4. 在側邊欄按下顯示，並拖動**"設定LED在腳位13光源ON"**到主程式的"無線循環"方塊中。

5. 在上方欄位中找到"Download"，彈出方塊上找到自己已註冊的Shield Prime旁按下"Download"按鈕，等到他在方塊下方顯示"Success"就成功了！

### 連接線路

1. 在板塊右方可以看到有一個**紅燈**，紅燈下方有三條電線腳位，用三條電線插入這三個腳位。

2. 在Shield Prime中間位置找到**13號腳位**，並跟著紅燈腳位插入對應的線條上，便大功告成。

3. 現在你應該可以看到紅燈正在亮起。

你的第一個ObjectBlocks專題就已經完成了，如果有任何不明白的地方可以在下方找到對應連接看一看教學影片。

那麼，讓我們做一些更大難度的專題吧！

## [練習]

我們需要怎樣做，才能展示出走馬燈的效果呢？（即紅燈亮、黃燈亮、綠燈亮、黃燈亮、紅燈亮，以此為一個循環）

## 參考及鏈結

### 參考
1. [如何用Google登入ObjectBlocks.cc]
2. [如何連接ShieldPrime到自己賬號]
3. [如何開啟新ObjectBlocks專題]
4. [如何撰寫第一個ObjectBlocks程序]
5. [如何把程序下載到ObjectBlocks上]
6. [如何連接線路]

### 隨堂練習
[練習1]

<!-- links -->
[首頁]: ../../../../../index.md
[中華傳道會李賢堯紀念中學]: ../../index.md
[甚麼是物聯網（IoT）？]: https://zh.wikipedia.org/wiki/%E7%89%A9%E8%81%94%E7%BD%91
[IoT]: https://www.bakom.admin.ch/bakom/en/homepage/digital-switzerland-and-internet/internet/internet-of-things/_jcr_content/par/image/image.imagespooler.jpg/1561386168855/iot_2.jpg
[物聯網可以做什麼？]: http://www.youtube.com/watch?v=Q3ur8wzzhBU
[SmartCity]: https://miro.medium.com/max/768/1*oFQLs6z-B7o1NHKjpteSjw.png
[認識Arduino]: http://www.youtube.com/watch?v=Eicmn2U9sQE
[Arduino]: https://www.distrelec.ch/Web/WebShopImages/landscape_large/9-/01/arduino-a000066.jpg
[練習]: http://www.youtube.com/watch?v=IqGCrzSXqP8
[如何用Google登入ObjectBlocks.cc]: ./resource/setup-a.flv
[如何連接ShieldPrime到自己賬號]: ./resource/setup-b.flv
[如何開啟新ObjectBlocks專題]: ./resource/software-a.flv
[如何撰寫第一個ObjectBlocks程序]: ./resource/software-b.flv
[如何把程序下載到ObjectBlocks上]: ./resource/software-c.flv
[如何連接線路]: ./resource/hardware-a.mp4
[練習1]: https://forms.gle/S3QCgG3rAKCxDGL39