# Digital Signal Processing: HMM Training and Testing with the HTK toolkit
* Construct a digital monophone recognizer with the HTK toolkit.
* See "problem_description.pdf" for more details.


## Implementation
* Modified from: [Baseline model and script](http://speech.ee.ntu.edu.tw/homework/DSP_HW2-1/dsp_hw2-1.zip)
* In this work the following files are modified:
    - **lib/proto**: increase state number
    - **lib/mix2_10.hed**: increase number of Gaussian mixtures
    - **03_training.sh**: increase training iteration  
    - **run.sh**: an additional script that runs the whole training and testing pipeline directly
* Implementation details are specified in "**[report.pdf](https://github.com/andi611/DSP_HTK_Toolkit/blob/master/report.pdf)**".
* An testing accuracy of **97.76%** is achieved with this implementation.
* ![](https://github.com/andi611/DSP_HTK_Toolkit/blob/master/image/best.png)

 
## File Description
```
.
├── htk341_debian_x86_64/ ...   Compiled Binary Files of the HTK toolkit
├── src/ ...                    scripts to run the HTK toolkit, and model implementations
├── image/ ...                  Results
├── problem_description.pdf     Work spec
├── report.pdf                  Report describing this work
└── Readme.md                   This file
```


## Environment Setup
* Download the HTK tool: **[< Hidden Markov Model Toolkit (HTK 3.4.1) >](http://speech.ee.ntu.edu.tw/homework/DSP_HW2-1/htk341_debian_x86_64.tar.gz)**
```
$ wget http://speech.ee.ntu.edu.tw/homework/DSP_HW2-1/htk341_debian_x86_64.tar.gz
$ tar zxvf htk341_debian_x86_64.tar.gz
Place the unzip .tar folder under the same directory as ./src
```
* Or clone this repository:
```
$ git clone git@github.com:andi611/DSP_HTK_Toolkit.git
```
* Set path for the HTK tool with script:
```
└── src/
    └── bash set_htk_path.sh
```
* Refer to "problem_descriptiom.pdf pg.28" for more detail.


## Usage
### Run the whole training and testing pipeline automatically:
```
└── src/
    └── bash run.sh
```
### Run each script separately:
```
└── src/
    ├── bash 00_clean_all.sh
    ├── bash 01_run_HCopy.sh
    ├── bash 02_run_HCompV.sh
    ├── bash 03_training.sh
    └── bash 04_testing.sh
```

