# COVID19_AU

Data source: https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_Australia.  
The growth is clearly flatenning and will no longer fit the exponential curve, so I think the goverment's measures on controlling the virus spread is now working.  
政府措施生效，增长放缓，将不再符合指数增长模式。  
The webpage above is keep changing the table format everyday. It is too stupid to crawl a table that can only be used once, so this repository is no longer updated since 27/3/2020.  
数据来源网页格式变动频繁，2020年3月27日起不再更新。  

A simple linear regreesion model to predict the early growth of Australian corona virus cases. Update daily using Kalman filter (KF) data assimialtion technique.  
一个简单的线性回归模型预测澳洲初期新冠感染数。使用卡尔曼滤波方法融合每日更新数据以更新模型。  


Latest update on 26/3/2012. The growth in Vic is slower.  
最近更新于2020年3月26日。维州增速放缓。  

Raw data display a exponential growth:  
原始数据为指数增长:  
![](Out_Data/linear_au_2020_03_26.png)  

Data shows a linear growth under logarithmic scale. The model prediction and updating is below:  
数据在对数坐标下为直线增长。模型预测与更新如下图:  
![](Out_Data/log_kf_au_2020_03_26.png)  

Linear regression model were trained using data during Mar 11-20. KF updating started from Mar 20.  
3月11日-20日的数据用于拟合线性模型。卡尔曼滤波从3月20日开始更新模型。  

Legend:  
图例:   
    Continuous line: KF, the estimated number with KF data assimilation.  
    实线：使用使用线性模型与卡尔曼滤波更新的预测。  
    Dotted line: OL, the estimated number without KF data assimiltion (called "open-loop").  
    虚线：使用线性模型但不使用卡尔曼滤波的预测。  
    Cross: observation, the real reported number.  
    X：实际报道（观测）数。  

------------------
Note: Result before 25/3/2012 were fitted using data during Mar 8-15. KF updating started from Mar 14.  
注：3月25日前的预测使用3月8日-15日的数据用于拟合线性模型。卡尔曼滤波从3月14日开始更新模型。  