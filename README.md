# Faces-Recognition-based-on-Embedded-System
实现基于Infineon CY8CPROTO-062-4343W PSoC 6的开发板和PTC06摄像头的嵌入式端拍照和发送图像数据为TCP到云服务器的功能（Implementation of Infineon CY8CPROTO-062-4343W PSoC 6 based development board and PTC06 camera on the embedded side to take pictures and send image data as TCP to a cloud server） 
文档结构如下：The document structure is as follows:
camera/
├── source/                          # 源代码目录
│   ├── main.c                      # 主程序入口
│   ├── uart_hal.c                  # UART硬件抽象层
│   ├── z_wifi/                     # WiFi任务模块
│   │   └── wifi_task.c             # WiFi连接管理
│   ├── z_cam/                      # 摄像头任务模块
│   │   ├── cam_task.c              # 摄像头控制和网络传输
│   │   └── ptc06.c                 # PTC06摄像头驱动
│   └── z_inc/                      # 头文件目录
│       ├── app_cfg.h               # 系统配置参数
│       ├── wifi_task.h             # WiFi任务接口
│       ├── cam_task.h              # 摄像头任务接口
│       ├── ptc06.h                 # 摄像头驱动接口
│       └── uart_hal.h              # UART接口定义
├── image_server.py                  # Python图像接收服务器
├── Makefile                        # 编译配置文件
├── README.md                       # 项目说明文档
├── 专业名词及解释翻译              # 技术术语说明
├── 相关知识点                      # 技术知识总结
└── 项目总结报告.md                 # 本文档
