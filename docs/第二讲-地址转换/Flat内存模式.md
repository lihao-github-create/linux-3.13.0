# Flat内存模式

## 疑问

![1532220672055.png](image/1532220672055.png)


![1532220682312.png](image/1532220682312.png)

* 进程线性地址空间和逻辑地址空间什么区别？

![1532220726102.png](image/1532220726102.png)


![1532220753186.png](image/1532220753186.png)

* 内核初始化阶段设置GDT和IDT
* 设置GDT和IDT有专门的特权指令lgdt、lidt
* GDTR和IDTR都是48位寄存器：16bit偏移+32bit物理地址


## 实证

![1532220849299.png](image/1532220849299.png)

![1532222421943.png](image/1532222421943.png)

![1532222438920.png](image/1532222438920.png)

![1532222454086.png](image/1532222454086.png)

![1532222464395.png](image/1532222464395.png)

![1532222485605.png](image/1532222485605.png)

![1532223884545.png](image/1532223884545.png)

* 不管用户态还是内核态，CS都设置为[0,0xFFFF-FFFF]。因此，全局只有一个段flat模式
* 段基址就是都是0，本来线性地址 = 段基址+偏移量，但是段基址为0，那么线性地址=偏移量

![1532224478509.png](image/1532224478509.png)

![1532224492245.png](image/1532224492245.png)






## END
