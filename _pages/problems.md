---
layout: page
toc: false
title: Problems
sidebar: true
icon: fas fa-sort-numeric-down
order: 4
---
## FFT

### Problem

- Basic  - 1024-Point FFT Single Kernel Programming

    The basic requirement is to complete a 1k-Point FFT design based on  personal understanding using AIE API or AIE Intrinsic. 

    - AIE Emulation succeeded
    - The design report submitted

- Advanced  - Explore very large point FFT (8k ~ 64k points) design on VCK5000 

    - The system level emulation or the hardware run on VCK5000 succeeded
    - The design report submitted

### Scoring Rules 

- Using Performance Matrix to measure 

The following table shows an example:

| Point Size  | Number of AIE   | GSPS | Data Type | Twiddle Type |Power| GSPW 
|-------|--------|-------|---|---|---|---|
| 4K | 5 | 2 |cint16 |cint16|1100| 1.8|

- Using the same number of AIEs and the same input data type

The higher the sampling rate (GSPS), the shorter the calculation period, and the higher the throughput rate, the higher the score.

- Use different numbers of AIEs or different input data types

The larger the points of FFT, the better the scalability, and the more reasonable the utilization of AIE and PL resources, the higher the score.

### Supported FFT Development Flow 

The Vitis tool chain currently supports three types of development from bottom to top:

- [AIE Intrinsic](https://www.xilinx.com/htmldocs/xilinx2022_2/aiengine_intrinsics/intrinsics/index.html)
    - AI Engine supports the lowest level of development by intrinsic functions.
    - By restructuring the scalar application code with these intrinsic functions and vector data types as needed, you can implement the vectorized application code.

- [AIE API](https://www.xilinx.com/htmldocs/xilinx2022_2/aiengine_api/aie_api/doc/index.html)
    - The AIE API offers the aie::fft_dit class template that provides the building blocks to implement all the stages of the FFT decimation-in-time computation. 

- [Vitis DSP AIE Library](https://xilinx.github.io/Vitis_Libraries/dsp/2021.1/user_guide/L2/1-introduction.html#)
    - The DSP Lib contains FFT/iFFT solution. This is a single channel, decimation in time (DIT) implementation. 
    - It has configurable point size, data type, forward/reverse direction, scaling (as a shift), cascade length, static/dynamic point size, window size, interface api (stream/window) and parallelism factor. 

### Reference Design

- The Stockham Algorithm is used to implement FFT on the AIE.

- Different reference design with different level of start point using AIE API, AIE Intrinsic and Vitis DSP Library will be provided during training.

- The reference design developed by AIE intrinsic is for reference only. Entrants must make changes or innovations based on the reference design.

- The reference design online documentation can be found [here]( https://docs.xilinx.com/r/en-US/xapp1356-fft-ai-engine). 


## Filter2D

### Problem

-  Basic  -  Vision 3X3 filter2D on 64x64 image

    Create the filter2D function with 3x3 kernel on 64x64 image using AIE API or AIE Intrinsic based on personal understanding

    - AIE Emulation succeeded
    - The design report submitted

-  Advanced - Image Signal Processing Pipeline on HD image

    Create high definition image processing pipeline design based on personal understanding. It is encouraged to fully use the Vitis Vision Library.

    - The system level emulation or the hardware run on VCK5000 succeeded
    - The design report submitted

### Scoring Rules

- Basic requirement

    With the same number of AIEs and the same input data type, teams with fewer storage resources and shorter computing cycles score higher.

- Advanced requirement

    The larger the design input image size (HD~4K), the higher the frame rate (FPS), the higher the score.

    The higher the innovation degree of the design, the more reasonable the application design of the basic image processing pipeline of the system, the higher the score.

### Reference Design

The reference design is from the Vitis Vision L2 AIE Library. The filter2D source code developed by AIE intrinsic can be found on the [Vitis Vision Library Github](https://github.com/Xilinx/Vitis_Libraries/blob/main/vision/L1/include/aie/imgproc/xf_filter2d_aie.hpp).



