# Design of Machine Elements Final Project
[TOC]
###### tags: `Coursework` `Mechanical` `Mechine Elements`

## Some Links
* [Course Website](http://pmsl.bime.ntu.edu.tw/courses/design-of-machine-elements/)
* [Google Docs](https://docs.google.com/document/d/1vFB1Jog2y-ZgbxmgvZF39MWlgbUp0rYZV7EQ9oap_9Y/edit?usp=sharing)
* [Google Slide](https://docs.google.com/presentation/d/1ceyyxf0taVJSSd-f3Po5F3HdduaNGuvH7w5CXtFe7RU/edit?usp=sharing)

- [MITSUBOSHI 皮帶設計 (JP)](https://tw.c.misumi-ec.com/book/MIB1_21/digitalcatalog.html?page_num=G-27)
- [MITSUBOSHI Design Manual V-Belt V844-E_DIN](https://www.mitsuboshi.com/dcms_media/other/V844-E_DIN.pdf)
- [MITSUBOSHI Manuals](https://www.mitsuboshi.com/english/support/catalog/)
- [MITSUBOSHI Manuals (JP)](https://www.mitsuboshi.com/support/catalog.html)
- [MISUMI - 圓形皮帶的選定方法](https://tw.misumi-ec.com/pdf/fa/2019/p2991.pdf)
![](https://i.imgur.com/8eBk2lZ.png)

* [200W伺服馬達套裝0.6N.m 3000轉 60法蘭](https://www.ruten.com.tw/item/show?21919402595221)


## Equations
$c^2=\frac{1}{4}[l-\pi(r_{1}-r_{2})^2]-(r_{1}-r_{2})^2$
$\alpha = 180 - 2 arcsin(\frac{D-d}{2c})$
$KW=\frac{Fv}{1000}=\frac{(P_{1}-P_{2})v}{1000}$
$\frac{P_{1}-mv^2}{P_{2}-mv^2}=e^{f\alpha}$
$a = \frac{P_{1}}{A}$

## Limit & Assumption
* Slope Gradient = 40°
* Wheel Dimension = 100 mm
* Speed = 1.5 m/s (about 5.4 km/hr) 
* Acceleration = 0.5 $m/s^2$
* Weight = 10 kg
* Rolling Resistance Coefficient $C_{rr}$ = 0.08 [Rolling Resistance](https://www.engineeringtoolbox.com/rolling-friction-resistance-d_1303.html)
* Torque
    * Load Torque (include friction load and gravitational load)
        * Gravitation Force: $10*9.8*\sin(40°)=62.99(N)$ ($mg\sin(\theta)$)
        * Friction Force: $10*9.8*\cos(40°)*0.08=6.01(N)$ ($mg\cos(\theta)*C_{rr}$)
    * Acceleration Torque (for the maximum acceleration rate)
        * Acceleration Force: $10*1.5=15(N)$ ($ma$)
    * Total Torque: $(62.99+6.01+15)*0.05=4.2(N*m)$
    * Motor Torque:
    $0.6(N*m)$
    * Total Torque(change): $(62.99+6.01+15)*0.05=4.2(N*m)$
* Power
    * $4.2*(1.5/0.05)=126(w)$ ($T*(V/r)$)
    

### Calculate Reference
* [Link](https://www.researchgate.net/post/How-can-we-calculate-the-required-torque-to-move-a-massive-object-by-means-of-gear-assembly)
The required tractive torque of the motor shall be equal to the tractive torque at wheel,  $T_{w}=F_{t}.r_{w}$  , (i.e. Tractive Torque =  Tractive Force x mean wheel radius).
Where,
$r_{w}$ = mean wheel effective radius
$F_{t}=F_{r}+F_{g}+F_{d}+F_{ie}$
$F_{r}$ = Tyre rolling resistance [滾動阻力](https://zh.wikipedia.org/wiki/%E6%BB%BE%E5%8B%95%E9%98%BB%E5%8A%9B) (can be in the form of  CrN - simplified and treated as independent of velocity) 
$F_{g}$ = forces due to gradient 坡度 (depending on slope angle, can be positive of negative)
$F_{d}$ = aerodynamics 空氣動力學 drag (as a function of air density, drag coefficient, vehicle cross sectional area, and squared of vehicle velocity)
$F_{ie}$ = equivalent inertial force (during acceleration) - (including linear and rotational inertias, due to vehicle mass and rotating component of gear train and wheels)
So you must determine the acceleration required to reach you designed speed.
And must also include overall transmission efficiency in order to get the right size of the motor.
Just to visualize;
for 1000 kg car and everything else constant;
on flat road, @ 25 km/h requires 1.0 kW power
on 5° gradient climbing, @ 25 km/h requires 6.9 kW power
on flat road,  accelerating @ 1.4 m/s2 (i.e. 0 - 25 km/h in 5 sec),  requires 10.6 kW power.


## Fatigue
### Rainflow Method 雨流法

## Simulation
### ANSYS
<iframe width="560" height="315" src="https://www.youtube.com/embed/FicB76ro6x8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube.com/embed/YznXPkxZiDY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube.com/embed/UTnK-LRyknY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
#### Basic
https://youtu.be/vnpq5zzOS48

### SOLIDWORKS
<iframe width="560" height="315" src="https://www.youtube.com/embed/Xmyryo9kVlc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube.com/embed/blVeZToVrn0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube.com/embed/p3YAdqpPxxI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube.com/embed/2pkH3_Eqsgc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Others
### Note 1
這堂課著重在幾何的分析 材質比較不重要
要分析什麼-緊邊鬆邊差異 應力分佈 摩擦力的分佈
得到分析結果之後要追求什麼-z.B.體積最小化當作最佳化的目標
傳遞的功率是皮帶輪很重要的議題

要傳遞的功率是多少
扭矩要提供多少
傳遞的扭矩是多少

下週的 proposal 先做一個案例
期末再延伸

### Note 2
1. 一邊輪設位移限制，另一邊設小的扭矩，因為 SOLIDWORKS 會跑到所有條件都滿足才會停止
2. 可能需要先用位移之類的方法讓皮帶輪有張力才能有摩擦力，用到多步驟的分析
3. 應該先用等效的概念只分析皮帶，手動算出一些值帶到皮帶或是半條皮帶上做分析

![](https://i.imgur.com/5ZKhgck.png)

### Note 3
![](https://i.imgur.com/5GnABau.png)
![](https://i.imgur.com/dbcIuXd.png)
![](https://i.imgur.com/IVPOdY2.png)


### Note 4
關於皮帶的受力分析，可以參考課本皮帶那一章節的內容或是廖老師的課程影片（應該是影片9與10）

皮帶主要是受到張力(P1, P2)，以及因為帶動輪子，會有磨擦力，以及在徑向方向的向心加速度。其中，所承受的最大應力將發生在P1或者P2的張力，取決於輪子是逆時針旋轉或者順時針旋轉，以及是主動輪還是被動輪。

當然超過這個最大應力，皮帶就會失效；因此可以去探討皮帶的材質，不同材質可承受的最大應力就不同。另外，是平面皮帶還是V型皮帶，在受力的分析也有些許不同。
因此，轉速則跟馬達所提供的功率有關，可以參考廖老師的影片中提到的例題。

關於載重，則可參考以下資訊，將跟馬達與軸有關（坡度的角度則是可以分解成鉛直方向與水平方向來看，或是我們可以先探討平面）
https://www.orientalmotor.com.tw/teruyo_det/teruyo_46/