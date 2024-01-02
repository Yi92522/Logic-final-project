# Logic-final-project
  
#### Input/Output unit:<br>
* 8x8 LED 矩陣，用來顯示遊戲畫面。下圖設定關卡後的初始畫面。<br>
<img src="https://github.com/Yi92522/Logic-final-project/blob/7220fed44bfaa38b179c2b89b793ae76f066fc45/logic%20image/IMG_2353.jpg" width="300"/><br>  
* 七段顯示器，用來顯示遊戲畫面。下圖設定關卡後的初始畫面。<br>
<img src="https://github.com/Yi92522/Logic-final-project/blob/bc1f7c69e0588522da605b2678374ed3c6919652/logic%20image/IMG_2354.jpg" width="300"/><br>
* 8x8 LED 矩陣，用來顯示遊戲畫面。下圖設定關卡後的初始畫面。<br>
<img src="https://github.com/Yi92522/Logic-final-project/blob/21304fb1d2855fb0c02c95206368c181325193e6/logic%20image/IMG_2355.jpg" width="300"/><br>
* 8x8 LED 矩陣，用來顯示遊戲畫面。下圖設定關卡後的初始畫面。<br>
<img src="https://github.com/Yi92522/Logic-final-project/blob/21688afcd2990a5e996e4636d9b90984f9998d3a/logic%20image/IMG_2356.jpg" width="300"/><br>
* 8x8 LED 矩陣，用來顯示遊戲畫面。下圖設定關卡後的初始畫面。<br>
<img src="https://github.com/Yi92522/Logic-final-project/blob/20384afb10d69a948ca92f7c89953617717a8579/logic%20image/IMG_2357.jpg" width="300"/><br>  
  
  
#### 功能說明:<br>  
在選擇完不同的關卡之後，按下發射鍵即可開始遊玩。  
透過按鍵左右移動底部可操控區域，去反彈發射的球來擊破關卡設置的磚塊。  
一次遊戲將會有三次機會，若球從底部落下的話將會扣除機會，若剩餘機會歸零即失敗。  
將球透過反彈擊破磚塊將會獲得分數，如果獲得8分即通關。  

#### 程式模組說明:<br>  
module final(  
					 input CLK,     
					 input sw_L,  
					 input sw_R,  
					 input shoot,  
					 input pause,  
					 input [3:0] back,    //背景變化  
					 output [7:0] lightR,  
					 output [7:0] lightG,  
					 output [7:0] lightB,  
					 output reg [2:0] whichCol,  //控制亮哪排  
					 output EN,  
					 output reg[7:0] win,  //亮燈得分  
                output reg beep,//音樂區  
                output reg a ,b,c,d,e,f,g  
);  

#### 說明各 I/O 變數接到哪個 FPGA I/O 裝置，例如: button, button2 -> 接到 4-bit SW<br>  
  
input sw_L,input sw_R,input shoot -> 接到 4-bit SW  
控制板子移動以及射擊  
  
input pause -> 接到 8 dipsw  
暫停遊戲  

input [3:0] back -> 接到 8 dipsw  
設定關卡  
  
output [7:0] lightR,output [7:0] lightG,output [7:0] lightB -> 接到 8x8 LED 矩陣  
顯示打磚塊遊戲畫面  
output reg [2:0] whichCol, output EN-> 接到 8x8 LED 矩陣  
控制燈亮的位置    
  
output reg[7:0] win -> 接到 LED 陣列  
顯示得分  
  
output reg a ,b,c,d,e,f,g -> 接到 七段顯示器  
顯示剩餘機會  
  
output reg beep -> 接到蜂鳴器  
播放背景音樂  
  

#### Demo video: (請將影片放到雲端空間)

<a href="https://drive.google.com/file/d/1MGVELfc3Qdur6w0UgtlaH6x8lO4o_wir/view?usp=sharing" title="Demo Video"><img src="https://github.com/Yi92522/Logic-final-project/blob/8aebc785107cb8c1d09a9b530c733b6ab9b4b9b9/logic%20image/IMG_2353.jpg" alt="Demo Video" width="500"/></a>
