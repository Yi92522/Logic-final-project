# Logic-final-project
功能說明:
紅色與藍色玩家對戰，先贏五球 或 在時間結束後最高分者獲勝。

程式模組說明:
module final(input CLK,
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

*** 請說明各 I/O 變數接到哪個 FPGA I/O 裝置，例如: button, button2 -> 接到 4-bit SW
*** 請加強說明程式邏輯
