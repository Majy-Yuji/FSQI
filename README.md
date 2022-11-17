# README

## Introduction

We want to developed a novel Fetal heart rate Signal Quality Index (FSQI) for signal quality classification from fetal heart rates collected from wearable devices. To achieve it, we developed our FSQI algorithm with the human-in-the-loop strategy to reduce the data annotation workload. Besides, we further proposed a post-processing technique to improve fine-grained detection. Finally, we introduced the application of integrating FSQI with existing FHR deceleration events detection algorithms.

## Data

FHR recordings each lasting 20 minutes using wearable devices. 

## Method

### Human-in-the-loop strategy

![](D:\project\fsqi\FSQI\pics\fw.png)

### FSQI algorithm

![](D:\project\fsqi\FSQI\pics\diagram.png)



### post-processing technique

![](D:\project\fsqi\FSQI\pics\Fine-grained Detection.png)

### Application in fetal deceleration events

![](D:\project\fsqi\FSQI\pics\improve.png)

## Results

### FSQI

|                | Predicted Low FSQI | Predicted High FSQI |
| :------------: | :----------------: | :-----------------: |
| True Low FSQI  |        2625        |          5          |
| True High FSQI |         18         |        17219        |

The confusion matrix of using final FSQI for signal quality classification. The overall accuracy is 99.8842%.

### FSQI in fetal deceleration events

![](D:\project\fsqi\FSQI\pics\11.png)

The red rectangle represents bad quality segments, the yellow rectangle represents deceleration events.

## Paper Link

[Signal Quality Index for the Fetal Heart Rates: Development and Improvements for Fetal Monitorin](https://authors.elsevier.com/sd/article/S095741742202262X)

## Example Description

`11.txt` is the original data after linear interpolation to 4HZ

`11.csv` is the deceleration event time identified by WMFB method in MATLAB toolbox

`example.ipynb` is the core code, which can be run directly