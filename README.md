# ML 台大線上課程筆記
##  Introduction of Machine Learning
### Learning Map
![](https://i.imgur.com/AkGWn7q.png)
* scenario : 意思為學習的環境，一般來說我們是無法去決定學習的環境的，如果再沒有data的情況下我們會採用Reinforcement Learning，如果有的話我們就會使用Supervised Learning，甚麼樣的環境下，我們該採用何種方式，這是AI工程師所需要的。
* task :　為需要解決的問題，隨著我要處理的問題不同，有輸出scalar的regression、有輸出option的classification、有輸出Structured object的structured Learning。
* method :　也可以用model來表示，挑選一個好的function來解決task，同樣的task我們可以使用不同的method來解決，像是Linear model、SVM、K-NN.....。

### Supervised Learning(監督式學習)
監督式學習需要大量的training data，這些data告訴我們說，我要的function(功能為何?區分貓狗?)，以及輸入與輸出的關係(已經知道貓跟狗的樣貌)，但缺點在於監督式學習需要大量的label，我們必須教導機器甚麼才是正確的。
#### Regression(回歸)
Regression是ML中的task，我們樣machine找出來的function他的輸出，要是一個scalar，也就是數值
![](https://i.imgur.com/BbqrQcU.png)
#### Classification
Classification與Regression差別在於輸出的類型不同，Regression輸出的是數值，而Classification輸出又分兩種。
* Binary Classification（二元分類） :　是or否，像是gmail一樣可以幫你選出垃圾郵件。
![](https://i.imgur.com/zyRSYci.png)

* Multi-class Classification :　機器要去做一個選擇題，給他數個選項，每一個選項都是一個類別，他必須去作出正確得判斷。
![](https://i.imgur.com/vGwU3dt.png)

### <font color="red">上述所說的都是你要machine解的任務，接下來是解任務中的步驟，</font>第一步就是要選擇不同function set，選不同的function set就是選不同的model set，你也會獲得不一樣的結果。

#### model(function set)選擇模型
* Linear Model(線性模型) : 最簡單的模型。
* non-Linear Model(非線性模型) :　最常用的模型，也是這堂課將會細講的模型。
    1.Deep learning : 以alpha go 為例，輸入當前的棋局，輸出是下一步的落子位子，由於棋盤是19 x 19的，因此你可以把它看成為一個19 x 19的選擇題
    2.SVM
    3.Decision Tree
    4.K-NN

### Semi-supervised Learning(半監督式學習)
今天一樣要做貓和狗得分類問題，你有大量的unlabel的data，有少量的label的data，但你沒有力氣去告訴機器去告訴機器哪些是貓，哪些是狗，而在Semi-supervised Learning技術裡，這些沒有label的data，他也是對學習有幫助的，<font color="green">接下來的課堂將會介紹</font>
![](https://i.imgur.com/spacLKQ.png)

### Tranfer Learning(轉移學習)
這是另一個減少data量的方法，假設我要做貓和狗的分類問題，一樣只有少量label的data，但在大量的data中，有一些毫無相關的內容，他可以帶來甚麼樣的幫助，這就是Tranfer Learning要講的問題。
![](https://i.imgur.com/oox7lb9.png)

### Unsupervised Learning(非監督式的學習)
我們希望機器能夠學到無師自通，我們給機器看大量的文章，他能不能學會每一個詞彙的意思，假設我們丟入一個詞彙為apple，機器要告訴你apple是甚麼意思，另一個舉例是我們讓機器去動物園看大量的動物，他能不能自己創造一些動物，你的function的輸入，是某一段code(可能代表要輸出的圖片特性)，那他輸出就是一張圖片，你給機器看非常大量的圖片，你只有function的output沒有input，在這個情況下，機器要怎麼學會自己生成圖片，這是之後會再cover的問題。
![](https://i.imgur.com/yqEuV1E.jpg)

### Structure Learning
在Structure Learning裡面，我們要機器輸出的是一個有結構性的東西、複雜的物件，舉例來說我輸入的是聲音訊號，輸出是一個句子，輸入是中文，輸出是英文，你給機器看一張圖片，他要知道圖片中的每一個角色。
![](https://i.imgur.com/OGyrduq.png)

### Reinforcement Learning
我們並沒有告訴機器正確的答案是甚麼，機器最後只會得到一個分數，就是他做的好還是不好，舉例來說我們現在有一個聊天機器人，讓他跟進來的客戶聊天，講了半天之後，結果客戶掛了他的電話，機器就學到了剛剛做錯了，所以他要自己思考哪邊做錯了，<font color="red">Reinforcement Learning的重點在於它是從評價中去學習</font>。
![](https://i.imgur.com/9W5J4L0.png)

### 有興趣的朋友，可以上youtube找李宏毅教授的頻道，可以瞭解更詳細的內容。