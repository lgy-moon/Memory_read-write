In this design, the total capacity of the storage module is 2KB and the bit width is 32bit. Considering the power consumption, the storage space is divided into two memory blocks. Each block of memory is 1KB, which is 256*32bit size. The two pieces of memory are addressed in turn.

Function:
Load Byte:	      Byte数据装载，根据byte地址从memory读取出相应8bit字节，经过高位符号位扩展后形成一个32bit数输出
Load half word:   半字数据装载，根据半字地址（地址最低位为0）读取出相应16bit半字，经过高位符号位扩展后形成一个32bit数输出
Load word:        整字数据装载，根据字地址（地址最低2bit为0）读取出一个32bit数输出
Store Byte:	      Byte数据存储，将输入32bit数据的低8位根据byte地址存入存储器
Store half word:  半字数据存储，将输入32bit数据的低16位根据半字地址存入存储器
Store word:       整字数据装载，将输入32bit数据存入存储器
