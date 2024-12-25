# STM32F103移植Zbar算法，识别QRcode二维码工程

## 项目描述

本项目旨在将Zbar算法移植到STM32F103微控制器上，用于识别QRcode二维码。移植过程参考了相关论坛帖子，并对Zbar库中的内存管理函数进行了自定义替换，以适应STM32F103的资源限制。由于STM32F103的SRAM资源有限，本项目使用了外部SRAM来存储数据。

目前，项目中尚未集成摄像头获取图片的功能，因为STM32F103没有DCMI接口，驱动摄像头较为复杂且速度较慢。因此，在测试阶段，我们仅在工程中定义了一个灰度图像数组，并将该数组送入Zbar库进行二维码检测。如果需要配合摄像头使用，只需将摄像头获取的图片数组送入Zbar库进行识别即可。

## 主要功能

- **Zbar算法移植**：成功将Zbar算法移植到STM32F103微控制器上。
- **自定义内存管理**：替换了Zbar库中的内存管理函数，以适应STM32F103的资源限制。
- **外部SRAM使用**：使用外部SRAM来扩展内存，以满足Zbar算法的需求。
- **灰度图像数组测试**：在工程中定义了一个灰度图像数组，用于测试二维码识别功能。

## 未来工作

- **集成摄像头**：考虑使用其他方式驱动摄像头，将摄像头获取的图片送入Zbar库进行识别。
- **优化性能**：进一步优化算法和内存管理，提高二维码识别的速度和准确性。

## 注意事项

- 本项目目前仅支持灰度图像数组的二维码识别，尚未集成摄像头功能。
- 使用外部SRAM时，请确保硬件连接正确，并根据实际情况调整内存管理函数。

## 贡献

欢迎大家提出改进建议或提交代码，共同完善本项目。

## 下载链接

[STM32F103移植Zbar算法识别QRcode二维码工程](https://pan.quark.cn/s/9e1a721cfa64)