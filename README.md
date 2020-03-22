# COVID19_AU
A simple linear regreesion model to predict Australian corona virus cases. Update daily using Kalman filter data assimialtion technique.
Lattest update:

![](Out_Data/log_kf_au_2020_03_22.png)
Linear regression model were trained using data during Mar 3-16. KF updating started from Mar 14.
Legend: 
    Continuous line: the estimated number with KF data assimilation.
    Dotted line: the estimated number without KF data assimiltion (called "open-loop").
    Cross: the real reported number (observation).
