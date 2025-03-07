# func
```
H 最高價
HIGH 最高價
O 開盤價
OPEN 開盤價
L 最低價
LOW 最低價
C 收盤價
CLOSE 收盤價
VOL 成交量
VOLA 成交量(額) 						                                //返回該周期成交量,恒生指數與國企指數返回成交額
AMOUNT 成交額
TOTALAMOUNT 當天累計的成交額			                                //返回當天累計的成交額
TOTALVAL 								                                //返回當天累計的成交量
PERIOD 周期類型 						                                //取得周期類型,結果從0到18,依次分別是1/5/15/30/60分鐘,日/周/月,多分鐘,多日/季/年,3分/120分/4小時/10分/20分/90分/3小時
DATE 日期 								                                //取得該周期從1900以來的的年月日, 用法:DATE,例如函數返回1000101,表示2000年1月1日,DATE+19000000後才是真正的日期值
TIME 時間(時分) 						                                //取得該周期的時分,適用於日線以下周期, 用法:TIME, 函數返回有效值範圍為(0000-2359)
TIME2 時間(時分秒)						                                //取得該周期的時分秒,適用於日線以下周期, 用法:TIME2,函數返回有效值範圍為(000000-235959)
YEAR 年份
MONTH 月份
WEEKOFYEAR 年內星期						                                //取得該周是年內第幾個周
WEEKDAY 星期							                                //取得該周期的星期數, 用法:WEEKDAY,函數返回有效值範圍為(1-7)
DAY 日期								                                //取得該周期的日期, 用法:DAY,函數返回有效值範圍為(1-31)
HOUR 小時								                                //取得該周期的小時數, 用法:HOUR,函數返回有效值範圍為(0-23),對於日線及更長的分析周期值為0
MINUTE 分鐘								                                //取得該周期的分鐘數, 用法:MINUTE,函數返回有效值範圍為(0-59),對於日線及更長的分析周期值為0
DATETODAY 轉換天數						                                //指定日期到1990.12.19的天數, 用法:DATETODAY(date),返回date到1990.12.19的天數.有效日期為(901219-1341231)
DAYTODATE 轉換日期						                                //求1990.12.19後第若幹天的日期, 用法:DAYTODATE(N),DAYTODATE(N).返回1990.12.19後第N天的日期.有效天數為(0-20000)
TIMETOSEC 當日秒數						                                //求指定時刻距0時有多長時間, 用法:TIMETOSEC(time),返回time時刻距0時有多長時間,單位為秒.有效時間為(0-235959)
SECTOTIME 轉換時間						                                //求0時後若幹秒是什麼時間, 用法:SECTOTIME(N),返回0時後N秒是什麼時間.有效秒數為(0-86399)
TOTALFZNUM 總分鐘數						                                //求該品種的每天的總交易分鐘數, 用法:TOTALFZNUM,返回當前品種的每天的總交易分鐘數,單位為分鐘.
FROMOPEN 當前離開盤總時間有多長 		                                //求該品種當前時刻已開盤有多長分鐘, 用法:FROMOPEN,返回當前時刻距開盤有多長時間(開市期間的相對時間),單位為分鐘.
DRAWNULL 無效數							                                //返回無效數, 用法:DRAWNULL
BACKSET 向前賦值						                                //屬於未來函數,將當前位置到若幹周期前的數據設為1, 用法:BACKSET(X,N),若X非0,則將當前位置到N周期前的數值設為1
ALIGNRIGHT 有效數據右對齊				                                //用法:ALIGNRIGHT(X)有效數據向右移動,左邊空出來的周期填充無效值
BARSCOUNT 有效數據周期					                                //求總的周期數, 用法:BARSCOUNT(X)第一個有效數據到當前的天數
BARSTATUS 數據位置狀態					                                //返回數據位置信息, 用法:BARSTATUS,1表示第一根K線,2表示最後一個數據,0表示中間位
CURRBARSCOUNT 到最後交易日的周期數		                                //求到最後交易日的周期數, 用法:CURRBARSCOUNT,求到最後交易日的周期數
TOTALBARSCOUNT 總的周期數				                                //求總的周期數, 用法:TOTALBARSCOUNT,求總的周期數
ISLASTBAR 是否為最後一個周期			                                //判斷是否為最後一個周期, 用法:ISLASTBAR,判斷是否為最後一個周期
BARSLAST 上一次條件成立到當前的周期數	                                //用法:BARSLAST(X),上一次X不為0到現在的天數
BARSNEXT 下一次條件成立到當前的周期數	                                //屬於未來函數,下一次條件成立到當前的周期數, 用法:BARSNEXT(X):下一次X不為0到現在的天數
BARSSINCEN N周期內第一個條件成立到當前的周期數 				            //用法:BARSSINCEN(X,N),N周期內第一次X不為0到現在的天數,N為常數
BARSSINCE 第一個條件成立到當前的周期數						            //用法:BARSSINCE(X),第一次X不為0到現在的天數
COUNT 統計													            //統計滿足條件的周期數, 用法:COUNT(X,N),統計N周期中滿足X條件的周期數
BARSLASTCOUNT 統計連續滿足條件的周期數						            //用法:BARSLASTCOUNT(X),統計連續滿足X條件的周期數
HHV 最高值													            //求最高值, 用法:HHV(X,N),求N周期內X最高值
HHVBARS	上一高點位置										            //求上一高點到當前的周期數, 用法:HHVBARS(X,N),求N周期內X最高值到當前周期數
HOD 求高值名次												            //用法:HOD(X,N),求當前X數據是N周期內的第幾個高值
LLV 最低點													            //求最低值, 用法:LLV(X,N),求N周期內X最低值
LLVBARS 上一低點位置										            //求上一低點到當前的周期數, 用法:LLVBARS(X,N),求N周期內X最低值到當前周期數
LOD 低值名次												            //求低值名次, 用法:LOD(X,N),求當前X數據是N周期內的第幾個低值
REVERSE 求相反數											            //用法:REVERSE(X)返回-X
REF 日前的													            //引用若幹周期前的數據(平滑處理), 用法:REF(X,A),引用A周期前的X值,A可以是變量,平滑處理:當引用不到數據時進行的操作.此函數中,平滑時使用上一個周期的引用值
REFV 日前的													            //引用若幹周期前的數據(未作平滑處理), 用法: REFV(X,A),引用A周期前的X值.A可以是變量.
REFX 日後的													            //屬於未來函數,引用若幹周期後的數據(未作平滑處理), 用法:REFX(X,A),引用A周期後的X值.A可以是變量
REFXV 日後的												            //屬於未來函數,引用若幹周期後的數據(平滑處理), 用法:REFXV(X,A),引用A周期後的X值.A可以是變量
REFDATE 日													            //引用自1900年以來指定日期的數據, 用法:REFDATE(X,A),引用A日期的X值
SUM 累和													            //求總和, 用法:SUM(X,N),統計N周期中X的總和
MULAR 累乘													            //求累乘, 用法:MULAR(X,N),統計N周期中X的乘積
TR 真實波幅													            //求真實波幅, 用法:TR,求真實波幅
SUMBARS 向前累加到指定值到現在的周期數						            //用法:SUMBARS(X,A):將X向前累加直到大於等於A,返回這個區間的周期數
MA 移動平均													            //返回移動平均, 用法:MA(X,N),X的N日移動平均,算法(X1+X2+X3+...+Xn)/N
SMA 簡單移動平均											            //返回簡單移動平均, 用法:SMA(X,N,M),X的N日簡單移動平均,M為權重,如Y=(X*M+Y'*(N-M))/N
TMA 遞歸移動平均											            //返回遞歸移動平均, 用法:TMA(X,A,B),A和B必須小於1,算法 Y=(A*Y'+B*X),其中Y'表示上一周期Y值.初值為X
MEMA 平滑移動平均											            //返回平滑移動平均, 用法:MEMA(X,N),X的N日平滑移動平均,如Y=(X+Y'*(N-1))/N
EMA 指數移動平均											            //返回指數移動平均, 用法:EMA(X,N),X的N日指數移動平均.算法:Y=(X*2+Y'*(N-1))/(N+1)
EXPMA 指數移動平均											            //返回指數移動平均, 用法:EMA(X,N),X的N日指數移動平均.算法:Y=(X*2+Y'*(N-1))/(N)
EXPMEMA 指數平滑移動平均									            //返回指數平滑移動平均, 用法:EXPMEMA(X,N),X的N日指數平滑移動平均
SMMA 平滑移動平均											            //返回平滑移動平均, 用法:SMMA(X,N),X的N日平滑移動平均.算法: Y=(X1+……+Xn)/N + [Xn - (X1+……+Xn)/N]/N
WMA 加權移動平均											            //返回加權移動平均, 用法:WMA(X,N),X的N日加權移動平均.算法:Yn=(1*X1+2*X2+...+n*Xn)/(1+2+...+n)
DMA 動態移動平均											            //求動態移動平均, 用法:DMA(X,A),求X的動態移動平均,算法:Y=A*X+(1-A)*Y',其中Y'表示上一周期Y值,A必須小於1
AMA 自適應均線值											            //求自適應均線值, 用法:AMA(X,A),A為自適應系數,必須小於1
XMA 偏移移動平均											            //屬於未來函數,返回偏移移動平均, 用法:XMA(X,N):X的N日偏移移動平均,用到了當日以後N/2日的數據
RANGE 介於某個範圍之間										            //在範圍之間, 用法:RANGE(A,B,C)表示A大於B同時小於C時返回1,否則返回0
TOPRANGE 當前值是近多少周期內的最大值						            //用法:TOPRANGE(X),X是近多少周期內X的最大值
LOWRANGE 當前值是近多少周期內的最小值						            //用法:LOWRANGE(X),X是近多少周期內X的最小值
FINDHIGH N周期前的M周期內的第T個最大值						            //用法: FINDHIGH(VAR,N,M,T),VAR在N日前的M天內第T個最高價
FINDHIGHBARS N周期前的M周期內的第T個最大值到當前周期的周期數            //用法:FINDHIGHBARS(VAR,N,M,T),VAR在N日前的M天內第T個最高價到當前周期的周期數
FINDLOW N周期前的M周期內的第T個最小值									//用法:FINDLOW(VAR,N,M,T),VAR在N日前的M天內第T個最低價
FINDLOWBARS N周期前的M周期內的第T個最小值到當前周期的周期數				//用法:FINDLOWBARS(VAR,N,M,T),VAR在N日前的M天內第T個最低價到當前周期的周期數
ZTPRICE 返回漲停價														//用法:ZTPRICE(REF(CLOSE,1),0.1),按10%計算得到在昨收盤基礎上的漲停價
DTPRICE 返回跌停價														//用法:DTPRICE(REF(CLOSE,1),0.1),按10%計算得到在昨收盤基礎上的跌停價
CONST 返回最後的值														//用法:CONST(A),取A最後的值為常量
FILTER 過濾連續出現的信號												//用法:FILTER(X,N):X滿足條件後,將其後N週期內的數據置為0,N為常量
CROSS 上穿																//兩條線交叉, 用法:CROSS(A,B)表示當A從下方向上穿過B時返回1,否則返回0
LONGCROSS 兩條線維持一定周期後交叉										//用法:LONGCROSS(A,B,N)表示A在N周期內都小於B,本周期從下方向上穿過B時返回1,否則返回0
UPNDAY 連漲																//返回是否連漲周期數, 用法:UPNDAY(CLOSE,M),表示連漲M個周期,M為常量
DOWNNDAY 連跌															//返回是否連跌周期, 用法:DOWNNDAY(CLOSE,M),表示連跌M個周期,M為常量
NDAY 連大																//返回是否持續存在X>Y, 用法:NDAY(CLOSE,OPEN,3),表示連續3日收陽線
EXIST 存在																//是否存在, 用法:EXIST(CLOSE>OPEN,10),表示前10日內存在著陽線
EVERY 一直存在															//一直存在, 用法:EVERY(CLOSE>OPEN,10),表示前10日內一直陽線
LAST 持續存在															//LAST(X,A,B):持續存在, 用法:LAST(CLOSE>OPEN,10,5),表示從前10日到前5日內一直陽線
NOT 取反																//求邏輯非, 用法:NOT(X)返回非X,即當X=0時返回1,否則返回0
IF 條件判斷 															//根據條件求不同的值, 用法:IF(X,A,B),若X不為0則返回A,否則返回B
IFF 條件判斷															//根據條件求不同的值, 用法:IF(X,A,B),若X不為0則返回A,否則返回B
IFN 條件反判斷															//根據條件求不同的值,同IF判斷相反, 用法:IFN(X,A,B),若X不為0則返回B,否則返回A
VALUEWHEN 條件跟隨														//用法:VALUEWHEN(COND,X),當COND條件成立時,取X的當前值,否則取VALUEWHEN的上個值
MAX 較大值																//求最大值, 用法:MAX(A,B),返回A和B中的較大值
MIN 較小值																//求最小值, 用法:MIN(A,B),返回A和B中的較小值
ACOS 反余弦值															//用法:ACOS(X),返回X的反余弦值
ASIN 反正弦值															//用法:ASIN(X),返回X的反正弦值
ATAN 反正切值															//用法:ATAN(X),返回X的反正切值
COS 余弦值																//用法:COS(X),返回X的余弦值
SIN 正弦值																//用法:SIN(X),返回X的正弦值
TAN 正切值																//用法:TAN(X),返回X的正切值
EXP 指數																//用法:EXP(X),為e的X次冪
LN 自然對數																//求自然對數, 用法:LN(X),以e為底的對數
LOG 對數																//求10為底的對數, 用法:LOG(X),取得X的對數
SQRT 開方																//開平方, 用法: SQRT(X),為X的平方根
ABS 絕對值																//求絕對值, 用法:ABS(X),返回X的絕對值
POW 乘冪																//用法:POW(A,B),返回A的B次冪
CEILING 向上舍入														//用法:CEILING(A),返回沿A數值增大方向最接近的整數
FLOOR 向下舍入															//用法:FLOOR(A),返回沿A數值減小方向最接近的整數
INTPART 取整															//用法:INTPART(A),返回沿A絕對值減小方向最接近的整數
BETWEEN 介於某個範圍之間												//用法:BETWEEN(A,B,C),表示A處於B和C之間時返回1,否則返回0
FRACPART 小數部分														//用法:FRACPART(X),返回X的小數部分
ROUND 四舍五入															//用法:ROUND(X),返回X四舍五入到個位的數值
ROUND2 四舍五入															//用法:ROUND2(X,N),返回X四舍五入到N位小數的數值
SIGN 取符號																//用法:SIGN(X),返回X的符號.當X>0,X=0,X<0分別返回1,0,-1
MOD 取模																//用法:MOD(M,N),返回M關於N的模(M除以N的余數)
RAND 取隨機數															//用法:RAND(N),返回一個範圍在1-N的隨機整數
AVEDEV 平均絕對方差														//AVEDEV(X,N),返回平均絕對偏差
DEVSQ 數據偏差平方和													//DEVSQ(X,N),返回數據偏差平方和
FORCAST 線性回歸預測值													//FORCAST(X,N),返回線性回歸預測值
SLOPE 線性回歸斜率														//SLOPE(X,N),返回線性回歸斜率
STD 估算標準差															//STD(X,N),返回估算標準差
STDP 總體標準差															//STDP(X,N),返回總體標準差
VAR 估算樣本方差														//VAR(X,N),返回估算樣本方差
VARP 總體樣本方差														//VARP(X,N),返回總體樣本方差
COVAR 協方差															//COVAR(X,Y,N),返回X和Y的N周期的協方差
RELATE 相關系數 														//RELATE(X,Y,N),返回X和Y的N周期的相關系數
VOLAT 歷史波動率														//VOLAT(X,N),返回歷史波動率
IV 引伸波幅																//返回歷史隱含波動率，僅在美股期權的分時、日k周期下可用
SAR 拋物轉向															//拋物轉向, 用法:SAR(N,S,M),N為計算周期,S為步長,M為極值
SARTURN 拋物轉向點														//SARTURN(N,S,M),N為計算周期,S為步長,M為極值,若發生向上轉向則返回1,若發生向下轉向則返回-1,否則為0
ZIG 之字轉向															//用法:ZIG(K,N),當價格變化量超過N%時轉向,K表示0:開盤價,1:最高價,2:最低價,3:收盤價,其餘:陣列資訊
ZIGA 之字轉向															//用法:ZIGA(K,X),當價格變化超過X時轉向,K表示0:開盤價,1:最高價,2:最低價,3:收盤價,其餘:陣列資訊
PEAK 波峰值																//波峰值, 用法:PEAK(K,N,M)表示之字轉向ZIG(K,N)的前M個波峰的數值,M必須大於等於1
PEAKBARS 波峰位置														//用法:PEAKBARS(K,N,M)表示之字轉向ZIG(K,N)的前M個波峰到當前的週期數,M必須大於等於1
TROUGH 波谷值															//用法: TROUGH(K,N,M)表示之字轉向ZIG(K,N)的前M個波谷的數值,M必須大於等於1
TROUGHBARS 波谷位置														//波谷位置, 用法:TROUGHBARS(K,N,M)表示之字轉向ZIG(K,N)的前M個波谷到當前的週期數,M必須大於等於1
DRAWKLINE 繪制日線														//用法: DRAWKLINE(HIGH,OPEN,LOW,CLOSE),以HIGH為最高價,OPEN為開盤價,LOW為最低,CLOSE收盤畫K線
STICKLINE 柱狀線														//用法: STICKLINE(COND,PRICE1,PRICE2,WIDTH,EMPTY),當COND條件滿足時,在PRICE1和PRICE2位置之間畫柱狀線,寬度為WIDTH,EMPTH為0畫實心柱,-1畫虛線空心柱,否則畫實線空心柱
PLOYLINE 折線段															//用法: PLOYLINE(COND,PRICE),當COND條件滿足時,以PRICE位置為頂點畫折線連接
DRAWICON 圖標															//用法: DRAWICON(COND,PRICE,TYPE),當COND條件滿足時,在PRICE位置畫TYPE號圖標(TYPE為1--41)
DRAWTEXT 文字															//用法: DRAWTEXT(COND,PRICE,TEXT),當COND條件滿足時,在PRICE位置書寫文字TEXT
DRAWNUMBER 畫數字														//用法：DRAWNUMBER(COND,PRICE,NUMBER,OFFSET1,OFFSET2)，當COND條件滿足時，在PRICE位置畫數字。OFFSET1是水平方向偏移量，OFFSET2是垂直方向偏移量。
DRAWBAND 畫帶狀線														//用法: DRAWBAND(VAL1,COLOR1,VAL2,COLOR2),當VAL1>VAL2時,在VAL1和VAL2之間填充COLOR1;當VAL1<VAL2時,填充COLOR2,這裏的顏色均使用RGB函數計算得到
FILLRGN 填充區域														//用法: FILLRGN(VAL1,VAL2,COND,COLOR),當COND條件滿足時,用COLOR顏色填充VAL1到VAL2之間的區域
DRAWLINE 直線段															//屬於未來函數,繪製直線段, 用法:DRAWLINE(COND1,PRICE1,COND2,PRICE2,EXPAND),當COND1條件滿足時,在PRICE1位置畫直線起點,當COND2條件滿足時,在PRICE2位置畫直線終點,EXPAND為延長類型
COLOR 自訂色															//格式為COLOR+“RRGGBB”：RR、GG、BB表示紅色、綠色和藍色的分量,每種顏色的取值範圍是00-FF,采用了16進制
COLORBLACK 黑色
COLORBLUE 藍色
COLORGREEN 綠色
COLORCYAN 青色
COLORRED 紅色
COLORMAGENTA 洋紅色
COLORBROWN 棕色
COLORLIGRAY 淡灰色
COLORGRAY 深灰色
COLORLIBLUE 淡藍色
COLORLIGREEN 淡綠色
COLORLICYAN 淡青色
COLORLIRED 淡紅色
COLORLIMAGENTA 淡洋紅色
COLORYELLOW 黃色
COLORWHITE 白色
LINETHICK 線性粗細 														//格式“LINETHICK+(1-9),參數的取值範圍在1—9之間,“LINETHICK1”表示最細的線,而“LINETHICK9”表示最粗的線
STICK 柱狀線															//畫柱狀線畫彩色柱狀線。
COLORSTICK 彩色柱狀線													//數據為正數時，向上畫紅色柱狀線，反之向下畫綠線
VOLSTICK 成交量柱狀線													//當股價上漲時顯示紅色空心柱，則顯示綠色實心柱
LINESTICK 同時畫出柱狀線和指標線										//同時畫出柱狀線和指標線
CROSSDOT 小叉線															//畫小叉線
CIRCLEDOT 小圓圈線														//畫小圓圈線
POINTDOT 小圓點線														//畫小圓點線
DOTLINE 虛線															//畫虛線
NODRAW 空線條															//不畫該線
+ 加
- 減
* 乘
/ 除
< 小於
> 大於
<= 小於等於
>= 大於等於
= 等於
!= 不等於
<> 不等於
AND 並且
OR 或者
&& 並且
|| 或者
( 括號
) 反括號
: 輸出
:= 賦值
; 語句結束
CAPITAL 當前流通股本
```
