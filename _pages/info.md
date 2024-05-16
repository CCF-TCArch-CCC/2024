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

<p align="middle">
    <img src="{% link media/qrcode.jpg %}" width="300" class="center">
</p>

## Rules

* Complete one of the two questions in the competition, and the top 5 with the highest total score will enter the final

* If both works are completed, the works with higher degree of completion shall be selected for total score

* Finalist entries should be open sourced at CCF-CCC@Github

## Scoring Criteria

* Performance score 40% (see [Problems]({% link _pages/problems.md %}))

* Design Report 40%

  * System architecture reasonable degree 20%

      - Use computing resources such as AIE and PL properly

      - The design of hardware architecture reasonable degree and performance optimization

  * Architecture Analysis and Innovation 20%

      - Present the strengths and weaknesses of the new architecture and suggest improvement ideas

      - Propose suitable application scenarios for this architecture

      - Explore the performance limits of the design

* Field defense 20%

## Target Platform

The 2023 contest will use the [VCK5000 Versal ACAP PLATFORM](https://www.xilinx.com/products/boards-and-kits/vck5000.html).

<p align="middle">
    <img src="{% link media/vck5000.png %}" width="300" class="center">
</p>

## Other Info

### AI Engine Introduction

AI Engines are an array of very-long instruction word (VLIW) processors with single instruction multiple data (SIMD) vector units that are highly optimized for compute-intensive applications.

- An AI Engine kernel is a C/C++ program which is written using **native C/C++ language, AI Engine API and specialized intrinsic functions** that target the VLIW scalar and vector processors. 

- The AI Engine kernel code is compiled using the **AI Engine compiler (aiecompiler) that is included in the Vitis™ core development kit**. The AI Engine compiler compiles the kernels to produce ELF files that are run on the AI Engine processors.

- AI Engine supports **specialized data types and API functions for vector programming**. By restructuring the scalar application code with these API functions and vector data types as needed, you can implement the vectorized application code. 

- The AI Engine compiler takes care of mapping API functions to **operations, vector or scalar register allocation and data movement, automatic scheduling, and generation of microcode** that is efficiently packed in VLIW instructions.

The AMD official tutorial is provided [here](https://github.com/Xilinx/xup_aie_training): https://github.com/Xilinx/xup_aie_training. 

### Frequently Asked Questions
  * [FAQs]({% link _pages/faq.md %})

### Previous Contest Winning Designs

  * 2022: https://github.com/xupsh/ccc
  * 2021: https://github.com/xupsh/ccc2021


