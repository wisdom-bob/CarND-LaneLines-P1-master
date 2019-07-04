# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

1. Describe the pipeline
灰度化，高斯滤波，canny算子获取边缘（设定高阈值捕捉边缘，低阈值用于连接补充边缘），再基于感兴趣区域提取边缘，在通过hough变换（设定最短线段和线段间隔，角度等）准确抓取边缘线段，从而绘制车道线。
