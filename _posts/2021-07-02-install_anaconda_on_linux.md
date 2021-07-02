---
layout: post
title: "How to Install Anaconda on Linux"
date:   2021-07-02
tags: [configuration]
comments: true
author: yiki
---

- Linux (CentOS):
    - Get installation link for Linux system from [anaconda official site](https://www.anaconda.com/products/individual#linux)
    - `wget https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh`
    - `bash ./Anaconda3-2020.11-Linux-x86_64.sh`
    - change the installation path to `/your_own_path/anaconda3`
    - Add PATH to /.bashrc file: 
        - `vi ~/.bashrc`
        - add `export PATH=/your_own_path/anaconda3/bin:$PATH` to the last line of `.bashrc` file
        - `source ~/.bashrc`
        - type `conda` to see if it works
    - Add essential channels
        - `conda config --add channels conda-forge`
        - `conda config --add channels r`
    - Create an environment called `r4`
        - `conda create -n r4 r-essentials r-base`
        - check what versions of R are available: `conda search R`
        - install R 4.0:  `conda install R=4.0`