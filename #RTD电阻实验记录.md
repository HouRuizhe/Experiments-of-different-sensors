​		#RTD电阻实验记录

##一、 实验器材

NI ELVISII+，ELVISBOX，RTD热电阻实验模块一个，PT100热电阻一根，PT1000热电阻一根，杜邦线四组。

\【**基本性能指标**\】

**备选电阻**

*阻值：200Ω，300Ω，500Ω，1kΩ，2kΩ

*公差等级1%，1/8W

**恒流源电路**

*电流范围 12.5、8.3、5、2.5、1.25

*电流精度：线性 

*最大负载： 最大负载： 960Ω（ Ri=200Ω）， 1440Ω（ Ri=300Ω）， 2.4KΩ（Ri=500ΩΩ）， 4.8KΩ（ Ri=1KΩ）， 9.6KΩ（ Ri=2KΩ）

**分压电路**

*总电压 5V

*下拉电压：200Ω、 300Ω、 500Ω、 1K Ω、 2K Ω

**PT100、PT1000热电阻Ÿ** 

*参数 A=3.92847×10-3/℃， B=-6×10 -7/℃， C=-4.22×10-12/℃。

*测温范围 测温范围 ：-190 ℃-630℃

 

 

##二、 实验步骤

###\（一\）实验准备

\【**ELVISbox准备**\】

1. 在桌上放置好NI ELVISII+，连接好电源线，再用USB线将其与电脑连接起来。（注意保证仪器上的两个开关均是关闭的）

2. 不用面包板，直接将ELVISBOX水平地插入NI ELVISII+对应的槽口上，注意下方也要卡入相应的卡槽内。

3. 将电源插头插入插座后，相继打开平台上的两个电源开关（分别在平台上方插头右侧和平台正面右上方）。接通后，平台正面右上方的“PROTOTYPING BOARD”处的POWER绿色指示灯会亮，并在一至两秒后“READY”黄色指示灯会亮；并且ELVISbox上右上方的“+15V”“-15V”“+5V”处的绿色指示灯也会亮起。在电脑上打开NI MAX界面，在“设备连接”里会显示“NI ELVISII+”，表示连接成功。之后关闭平台电源。

 

\【**模块准备**\】

4. 关闭平台电源，插上RTD热电阻实验模块，开启平台电源，此时可看到模块左上角绿色的电源指示灯亮。

   ![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEB5.tmp.jpg)



 

\【**软件准备**\】

5. 打开nextpad，点击右上角的“配置”图标，在配置界面中选择“加载”；

   ![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEC6.tmp.jpg)

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEE6.tmp.jpg) 



6. 在文件保存路径下，找到ELVISbox_Product Documentation_V1.0文件夹中的“nextmodule”文件夹，打开“nextsense”文件夹，再选择“RTD热电阻实验.nex”文件，并点击确定，等待系统自动加载完成；

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEE7.tmp.jpg)

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEE8.tmp.jpg)



7. 加载完成后，点击窗口下方正中央的按钮即可返回主界面，在主界面的下方便有一行正方形的图标，可查看已安装的实验；

8. 运行RTD热电阻实验应用程序：在nextpad主界面中选择RTD热电阻实验图标，双击进入实验。

   ​                   ![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEE9.tmp.jpg)

   

9. 在“传感器实验”界面的右边点击“Refresh”按钮，听到继电器弹片吸合的声音（“嘀嘀”声），并在下面的显示框内有显示“Dev 1”,开始进行试验。若没有吸合音，请查看ELVIS设备是否选择正确以及线缆是否正确连接。

 

###\（二\）开始实验

用万用表测量RTD热电阻实验模块“备选电阻”区域中的200Ω、300Ω、500Ω、1KΩ、2KΩ，并记录下值，以备后续测试使用。

**Tip**：备选电阻存在一定的公差，因此为了增加后续测量的准确性，需要对实验模块上的备选电阻进行测量。

####完成手动测量实验

\【**恒流源法测量**\】

软件切换到“仿真与测量”选项卡

**Step1**：用万用表对实验模块上的200Ω备选电阻进行测量，测量后在“备选电阻校准”一栏中，选择测量电阻后将实际测量值写入Ri，并点击更改按钮。

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEFA.tmp.jpg)

*Tip*：只有将用万用表实际测得的备选电阻阻值写入并确定更改后，在后续实验中所有需要用到Ri电阻的地方才会自动应用该值，减小实验误差。

|      |                                                              |
| ---- | ------------------------------------------------------------ |
|      | ![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEFB.tmp.jpg) |

**Step2**:用杜邦线将200Ω备选电阻连接到恒流源电路中Ri位置。将RTD热电阻连接到实验模块上的绿色螺丝拧线端子上，并拧紧。如图所示。

**Step3**:将万用表红黑表笔分别放置在实验模块恒流源法区域的VCC端和GND端，测量VCC和GND之间的电压，并将其填入电压测量部分。

*Tip*：此处也需手动测量并填写，同样会影响后续实验中软件恒流源/分压法自动测量选项卡中的计算结果。

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEFC.tmp.jpg) 

**Step4**：【伏安特性的手动测量】保持RTD热电阻工作温度不变，更换Ri电阻值，使用万用表手动测量Vt，通过计算获得在不同电流情况下的RTD热电阻的阻值。通常，在同一温度下，RTD热电阻的阻值基本不会随着电压或者电流的更改而改变。

（i=Vcc/Ri, Rt=Vc/i）

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEFE.tmp.jpg)

**Step5**：【R-T特性的手动测量】保持Ri不变，改变RTD热电阻工作温度值，使用万用表测量Vt，计算RTD热电阻阻值Rt，并借助特性曲线图中的游标值估算对应温度。

 ![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAEFD.tmp.jpg)

\【**分压法测量**\】

重复\【恒流源测量\】中的步骤

i=VRI/Ri=(VCC-Vt)/Ri, Rt=Vt/i

 

*Tip*：被测传感器PT100和PT1000的电阻值相差较大，因此在实验仿真阶段可以尝试PT100、PT1000与各种阻值Ri的组合。从测量结果可以看出，当Ri与传感器阻值接近时，Vt值正好处在VCC/2的区域，有助于测量的准确性。

在实际测量时，出于传感器保护以及测试准确性的考虑，在使用PT100测试时，请选用200Ω、300Ω、500Ω的备选电阻，使用PT1000时，请选用1KΩ、2KΩ的备选电阻。

 

####完成自动测量实验

软件切换到“自动测量”选项卡

 \【**恒流源实验**\】

**Step1**：用杜邦线将 200Ω备选电阻连接到恒流源路中Ri位置。将 RTD 热电阻连接到实验模块上的绿色螺丝拧线端子。见图 6-1。

**Step2**：在自动测量选项卡中恒流模式，将电路图中的电阻选择为200Ω ，并选好RTD热电阻的类型。如图 6-2所示。

**Step3**：点击恒流源界面右上角运行按钮，软件界面将通过测量到的Vt值，计算出电流、电阻和温度值。观察温度为当前温度，用手捏住RTD热电阻，观察曲线，有温度变化过程，最终曲线稳定后，观察温度接近体温温度，停止运行程序。

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAF0F.tmp.jpg)



\【**分压法实验**\】

**Step1**：用杜邦线将1K备选电阻连接到分压法电路中Ri位置。将RTD热电阻连接到实验模块上的绿色螺丝拧线端子。如图所示。



![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAF10.tmp.jpg)

**Step2**：在自动测量选项卡中选中分压模式，将电阻选择为1K。如图所示。

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAF11.tmp.jpg) 

**Step3**：将万用表红黑表笔分别放置在实验模块分压法区域的VCC端及GND端，测量VCC和GND之间的电压，并将其填入电压测量部分。

![img](file:///C:\Users\lenovo\AppData\Local\Temp\ksohtml\wpsAF12.tmp.jpg) 

**Step4**：点击分压法界面的运行按钮，软件界面将通过测量到的Vt值，计算出电流、电阻和温度值。观察温度为当前温度，用手捏住RTD热电阻，观察曲线，有温度变化过程，最终曲线稳定后，观察温度接近体温温度，停止运行程序。

 

##三、 实验中存在的问题及解答

1. 在使用Pt1000和恒流源法手动测量的过程中，将200Ω、300Ω和500Ω的电阻作为Ri时，测得的Vt值是理论值的2倍，Rt阻值与理论值误差较大，导致测不准。

解答：因为恒流源法中，Ri一定时，流经Ri的电流是一定的，当Rt太大时，

2. 两种方法得到的0℃时的Rt值不等于1000或100Ω，在操作一切规范的前提下，原因可能是出厂时阻值便不是严格为1000或100Ω。

或是这里的运算放大器不是运算放大器，所以简单地用“虚短”“虚短”的规则本身就会存在误差。