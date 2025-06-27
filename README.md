# Faces-Recognition-based-on-Embedded-System
# 基于 Infineon CY8CPROTO-062-4343W 和 PTC06 的嵌入式图像采集与TCP上传实现  
**Implementation of Infineon CY8CPROTO-062-4343W PSoC 6 based development board and PTC06 camera on the embedded side to take pictures and send image data as TCP to a cloud server**

---

## 前面的话  
**Preface**

本项目旨在使用 Infineon CY8CPROTO-062-4343W 开发板配合 PTC06 串口摄像头，实现图像的本地采集和通过 TCP 协议上传至远程云服务器的功能。该项目涵盖嵌入式系统开发、串口通信协议解析、图像数据处理与网络传输等关键技术环节，适用于嵌入式图像采集与远程传输方向的学习与实践。

This project aims to use the Infineon CY8CPROTO-062-4343W development board in combination with the PTC06 serial camera to capture images locally and upload them to a remote cloud server via the TCP protocol. It involves key techniques including embedded system development, serial communication protocol parsing, image data processing, and network transmission. It is suitable for learning and practicing embedded image acquisition and remote transmission.

---

## 文档结构  
**Document Structure**

```plaintext
camera/
├── source/                          # 源代码目录 / Source code directory
│   ├── main.c                      # 主程序入口 / Main program entry
│   ├── uart_hal.c                  # UART硬件抽象层 / UART Hardware Abstraction Layer
│   ├── z_wifi/                     # WiFi任务模块 / WiFi Task Module
│   │   └── wifi_task.c             # WiFi连接管理 / WiFi connection management
│   ├── z_cam/                      # 摄像头任务模块 / Camera Task Module
│   │   ├── cam_task.c              # 摄像头控制和网络传输 / Camera control and network transmission
│   │   └── ptc06.c                 # PTC06摄像头驱动 / PTC06 Camera Driver
│   └── z_inc/                      # 头文件目录 / Header files directory
│       ├── app_cfg.h               # 系统配置参数 / System configuration parameters
│       ├── wifi_task.h             # WiFi任务接口 / WiFi task interface
│       ├── cam_task.h              # 摄像头任务接口 / Camera task interface
│       ├── ptc06.h                 # 摄像头驱动接口 / Camera driver interface
│       └── uart_hal.h              # UART接口定义 / UART interface definitions
├── image_server.py                 # Python图像接收服务器 / Python image receiving server
├── Makefile                        # 编译配置文件 / Build configuration file
├── README.md                       # 项目说明文档 / Project documentation
├── 专业名词及解释翻译              # 技术术语说明 / Technical terms and translation
├── 相关知识点                      # 技术知识总结 / Technical knowledge summary
└── 项目总结报告.md                 # 本文档 / This documentation
```
