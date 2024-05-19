---
layout: page
toc: false
title: Participant Info
short_title: Info
sidebar: true
icon: fa fa-calendar
order: 2
---

## Registration

* [Registration](https://www.wjx.top/vm/tbXtzkR.aspx# ) 

请点击以下链接或扫描二维码报名

组委会将根据报名信息通知培训时间

https://www.wjx.top/vm/mBrTh1g.aspx

<p align="middle">
    <img src="{% link media/CCC2024_qrcode.jpg %}" width="300" class="center">
</p>


## Rules

本赛题的评分主要包含两个部分，为推理速度和推理模型精度。其中推理速度评分占比70%，模型精度占比30%。

**推理速度：**

推理速度分为prompt处理速度和token生成速度。Prompt处理速度：是指模型接收输入的prompt（提示）并处理所有输入token，直到生成第一个输出token所需的时间，即Prefill速度。Token生成速度：是指模型在生成第一个输出token之后，继续生成后续token的速度，即Decode速度。本赛题采用生成128个token的平均速度作为decode速度。

本赛题采用指标tokens/s，在给定prompt中，推理速度越快越好。本赛题分别以参赛者最快运行时间 $Decode_{best}$ 、$Prefill_{best}$为基准，推理生成速度评判分数计算如下：

$$Runtime = 70\% * ({Decode \over 2*Decode_{best}} + {Prefill \over 2*Prefill_{best}})$$

**模型精度的评估指标：**

本赛题使用困惑度(PPL)作为模型精度的评估指标，以模型在给定语料困惑度$P_{best}$ 为基准，模型精度评估分数计算如下：

$$PPL = 30\% * ({P - P_{best} \over P_{best}})$$

综合两者评分即为总分:

$$Total = Runtime + PPL$$

**若发现试图通过多次提交等手段来获取testbench信息的行为，组委会有权取消该题成绩**

## 奖项

第一名 10,000元

第二名 5,000元

第三名 3,000元

证书：成绩前 10% 一等奖证书，11 - 25% 二等奖证书，26 - 40% 三等奖证书

优秀作品将有机会入选CCFChip大会论文集

## 竞赛组织

主办单位： CCF计算机体系结构专委会

承办单位： CCFChip竞赛组委会，上海交通大学 IPADS

