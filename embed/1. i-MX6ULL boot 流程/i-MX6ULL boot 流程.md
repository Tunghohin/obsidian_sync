## 1. boot 方式的选择

**通过修改 BOOT_MODE 引脚选择 boot 的类型**
![[Screenshot from 2023-10-01 16-28-20.png]]**然后通过修改 BOOT_CFGx 引脚选择 boot 模式**
![[Screenshot from 2023-10-02 01-30-05.png]]
详情可见底板核心原理图

**alpha Linux 的 boot 控制拨档开关**
![[Pasted image 20231001162309.png]]
![[Screenshot from 2023-10-02 01-40-01.png]]

## 2. IVT 和 BootData

I.MX6U 的最终可烧写文件组成:
```
IVT + BootData + Device Configuration Data + .bin
```
* 假设我们将首地址置于 0x87800000，IVT 的首地址为 0x87800000 - 0xc00(3KB)
* DCD (Device Configuration Data) 记录了启动时对各个寄存器初始化的方式

**IVT**

![[Screenshot from 2023-10-02 02-52-56.png]]