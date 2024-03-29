[首頁] > [中華傳道會李賢堯紀念中學]

# 2. 數碼輸入

還記得我們上堂課做了什麼嗎？沒錯，我們做了讓LED燈發光的程序。

在這堂課，我們會做一個有關數據輸入的程序，來模擬平時在室內開關燈光的動作。

> 重新連接ObjectBlocks
>
> 可以到<https://www.youtube.com/playlist?list=PL5YnldTAw9VSK-HDIeBLhvlWW4GA3lydb>重溫。

## 認識Sensor Shield

Sensor Shield 是一個端口排列裝置，他只是令Arduino的端口**重新分配**，而不需要再用其他的轉接口。

> Sensor Shield
![shield]

> LED燈
![led]

> 按鈕
![button]

## 認識變數

變數是什麼？

不知道大家有沒有在數學課學過方程式呢？一條方程式往往都會擁有至少一個**未知數**，而每個方程式的未知數都會**承載**著不同的數值。例如

```javascript
2 * x = 4 
Ans: x = 2
```

和

```javascript
x + 8 = 16 
Ans: x = 8
```

不同的是，數學的未知數的數值，是根據每條不同的方程式而得到的**固定**的數值。

而電腦程式上的變量，是可以根據情況進行**變動**的。在通常情況下，假設我們定義了一個變量x：

```javascript
x = 2
```

這個x的數值是不會變化的。當我們**讀取**這些變量的時候，他永遠都會給出一樣的數值（2）。

但當我們重新**賦予**一個新的數值給變量x：

```javascript
x = 4
```

然後我們再讀取這個數值時，得到的答案就會不一樣，這就是變量的變動特性。

如果看了以上介紹還是不太明白的話，這裡有一個更加通俗易名的解釋：

```
變數等同於"盒子"，盒子可以承載著不同的東西。
我們可以探頭看看（讀取）盒子裡的東西，
也可以改變（賦予）盒子裡的東西。
```

## Arduino的變數

在Arduino建立和使用變數非常簡單。

1. 在程序導航中按下"變數"，並按下菜單中的"**建立變數**"
2. 這時會彈出一個對話框，需要輸入一個名稱，我們把它稱為**button**。

這樣，你再開變數導航的時候就多了一個button變數了。

## 按下著燈，鬆開關燈

1. 創建變數button
2. 讓變數button讀取按鈕腳位7
3. 設定LED腳位為4，並使他根據button變量的數據改變光源

![prog1]

## 切換式開關

剛剛我們已經做了一個數碼輸入裝置，但是這種裝置在日常生活中實用性不是非常大。接下來我們會做一個我們更加熟悉的切換式開關按鈕。

這種開關的邏輯是：
每次按下按鈕時
- 如果LED本來是關的話，開啟燈光。
- 如果LED本來是開的話，則關閉燈光。

> 關於數碼輸入
>
> 數碼信號只有兩個數值：0與1（開與關），按鈕是一個很好的數碼輸入例子。

我們需要用到"處理"導航中的兩個指令。

第一個是"當數碼訊號由強到弱執行"，這是一個**事件**。他讓我們可以在按下數碼輸入（按鈕）時執行一些動作，而這些動作會包含在這個方塊裡。這個事件指令在我們的練習中相當於在我們按下按鈕的那一刻去執行動作。
*（只有按下那一刻，其他時間都不會執行！）

第二個是"兩者間切換"。這個很容易理解，就是如果我們剛剛執行了上面的指令，我們現在就執行下面的指令，反之亦然。

![prog2]

我們這樣就寫完切換式開關的程式了。但是大家有沒有發現，按鈕又是按下去了，但是輸出並不如我們預期呢？

## 解決抖動問題

出現這個問題是因為按鈕有抖動問題，但要解決他，我們要先了解他。

抖動為什麼會出現呢？這是因為按鈕內部是由兩片金屬片組成。我們按按鈕就是把這兩片金屬片擠壓。當這兩片金屬片擠壓到一塊時，就會形成**閉合電路**。

但是由於金屬片的物理屬性，有時金屬片會**先閉合，再彈開，再閉合**，這樣重複幾次，這就是抖動。而這種現象的出現會導致程序以為我們快速的按了幾下按鈕，而如果抖動次數是偶數，就會導致沒有預期的輸出。

了解了什麼是抖動，解決的話就很簡單了。只需要在我們的button變量前增加**已去抖動**命令，程序就會讓金屬片先處於穩定狀態，再讀取他的狀態，這就避免了抖動問題了。

![prog3]

練習

1. 把按鈕換成障礙物傳感器（Optical Sensor）

> 注意！
>
> 母母線的插線對口一定要正確，否則裝置將會發出非常熱的溫度！

> 障礙物傳感器
>
> 障礙物傳感器的透明位置是紅外線發射區，而黑色位置是紅外線接收區。

2. [製作高階交通燈]
3. [製作感測障礙輪流亮起LED]

<!-- links -->
[首頁]: ../../../../../index.md
[中華傳道會李賢堯紀念中學]: ../../index.md
[shield]: ./resource/shield.jpg
[led]: ./resource/led.jpg
[button]: ./resource/button.jpg
[prog1]: ./resource/prog1.png
[prog2]: ./resource/prog2.png
[prog3]: ./resource/prog3.png
[製作高階交通燈]: https://www.youtube.com/watch?v=E2V2tYGU7Po
[製作感測障礙輪流亮起LED]: http://www.youtube.com/watch?v=O7c_zynOPEk