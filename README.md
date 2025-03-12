# slpash_manager
[J]Webページにスプラッシュ機能をつけてくれる実装スクリプト  
汎用スクリプト  
## What is this?  
Webページにようこそ画面(スプラッシュ画面)を簡単に実装できるスクリプト。 以下の設定がちゃんとできていれば動作すると思います。  
このスクリプトはこのリポジトリから入手する場合、MITライセンスです。  

1.実装 HTML  
```implement.html
<div id="splash" >
<div id="splashc"style="width: 80vw; display: flex;align-items: center;justify-content:center;">
<div class="C">
    <div class="A">  
        <div class="title">  
        <img src="./music.png" width="15%" height="15%">  
        <h1>製品名称</h1>   
         </div>  
         </div>  
         <div class="marks-container">
         <div class="marks-r-b2">
             <p>Rev.1.4(Release)-Caffeine_CSS Rev.4</p>  
         </div>  
         </div>
</div> </div>
</div>
<div id="main" class="fade-in">
<!--メインコンテンツをこのdiv内に全て格納します。-->
</div>


```
2. CSSの実装  
```implement.css

#main
{
    display: none; 
}
#splash
{
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content:center;
    z-index: 1000;
    background-image: url('./art.png'); 
            background-size: cover; 
            background-position: center;
            background-repeat: no-repeat;
}
.fade-in {
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

```
3. 最後に...
```zisso.html
<script src="./spmgr.js"></script>
```

機能 3秒でsplash画面を自動で隠し、メインコンテンツを表示します。(全てのメインコンテンツはmainをIDとしたdiv内に格納されている必要があります。)  

