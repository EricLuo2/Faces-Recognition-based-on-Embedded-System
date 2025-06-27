# Faces-Recognition-based-on-Embedded-System
实现基于Infineon CY8CPROTO-062-4343W PSoC 6的开发板和PTC06摄像头的嵌入式端拍照和发送图像数据为TCP到云服务器的功能（Implementation of Infineon CY8CPROTO-062-4343W PSoC 6 based development board and PTC06 camera on the embedded side to take pictures and send image data as TCP to a cloud server） 
文档结构如下：The document structure is as follows:
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
├── image_server.py                  # Python图像接收服务器 / Python image receiving server
├── Makefile                        # 编译配置文件 / Build configuration file
├── README.md                       # 项目说明文档 / Project documentation
├── 专业名词及解释翻译              # 技术术语说明 / Technical terms and translation
├── 相关知识点                      # 技术知识总结 / Technical knowledge summary
└── 项目总结报告.md                 # 本文档 / This documentation
```
