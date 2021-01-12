邏輯設計二十組 
資工二 108321020黃證瑋 108321023王承彥

題目: Google 恐龍
	實作出模仿google搜尋網站無網路時的小遊戲，藉由燈泡顯示出恐龍(用燈泡大略顯示)和障礙物(高一個至三個的垂直燈泡)，障礙物會往恐龍靠近，玩家要藉由我們設置的跳躍鍵使恐龍成功跳過障礙物，隨著時間增加障礙物的靠近速度會增加並同時計算恐龍跑的距離(每秒加一之類的)，直到恐龍撞到障礙物就停止。 

![3717](https://user-images.githubusercontent.com/61613341/104289205-d313ac00-54f3-11eb-8874-78f6f5ecc462.jpg)
左方第一個SWITCH為開始遊戲及重置分數否則他撞到障礙物不會暫停右方第一個是EN
![3719](https://user-images.githubusercontent.com/61613341/104289215-d60e9c80-54f3-11eb-9e50-4197a7c06a76.jpg)
左方第一個按鈕為跳躍鍵按下後恐龍便會跳起藉此躲避障礙物
![3718](https://user-images.githubusercontent.com/61613341/104289211-d5760600-54f3-11eb-9dc8-3f0a65531b0a.jpg)

 
D1~d8為距離顯示器，d8為最低位元，D1為最高位元，最大分數為256
程式解釋
一開始創造四個頻率給四個不同的物件，分別為暫停計數器、恐龍、藍色以及綠色障礙物。
divjump用來控制恐龍顯示即跳躍
divbobject用來控制障礙物的速度跟顯示
divcounter控制計數器的速度(分數)
divpause控制計數器的速度(暫停)
divfreq控制畫面顯示
以下為控制跳躍
  if(da <= 0)/恐龍Y軸
     forward=1;/方向為下
    if(forward == 0)/方向為上
    begin
     stateR[0][da]=1;
     stateR[0][da-1]=1;
     stateR[1][da]=1;
     stateR[1][da-1]=1;
     da=da-1;
    end
    else
    begin 
     stateR[0][da]=1;
     stateR[0][da-1]=1;
     stateR[1][da]=1;
     stateR[1][da-1]=1;
     da=da+1;
    end
    if(da >= 8)/方向改成向上
    begin
     forward = 0;
     da=7;
     stateR[0][da]=1;
     stateR[0][da-1]=1;
     stateR[1][da]=1;
     stateR[1][da-1]=1;
    end
  end

這是判斷失敗的條件
if(ob==0 || ob==1 || og==0 || og==1)(當障礙物進入恐龍的X軸)
 begin
   (判斷恐龍高度是否高於障礙物高度)
if((ob==0 && da-1>=6) || (ob==1 && da-1>=6) || (og==0 && da-1>=5) || (og==1 && da-1>=5))











