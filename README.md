# Logic-final-project
功能說明:  
在選擇完不同的關卡之後，按下發射鍵即可開始遊玩。  
透過按鍵左右移動底部可操控區域，去反彈發射的球來擊破關卡設置的磚塊。  
一次遊戲將會有三次機會，若球從底部落下的話將會扣除機會，若剩餘機會歸零即失敗。  
將球透過反彈擊破磚塊將會獲得分數，如果獲得8分即通關。  

程式模組說明:  
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

*** 說明各 I/O 變數接到哪個 FPGA I/O 裝置，例如: button, button2 -> 接到 4-bit SW  
  
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
  
*** 請加強說明程式邏輯  
