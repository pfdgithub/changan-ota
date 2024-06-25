# [二代CS55PLUS 系统升级包解包](https://tieba.baidu.com/p/7766465757)

## 时距曲线

/IncallUpgrade/HuOs/update.zip 被加密，解密后得到
![](https://tiebapic.baidu.com/forum/pic/item/641621fa43166d228b5074881b2309f79152d2f2.jpg?tbpicau=2024-07-06-05_06b039bed549a3cb35af374d4151a61c)

继续解 payload.bin得到
![](https://tiebapic.baidu.com/forum/pic/item/7adb3fae2edda3ccfd8462f344e93901233f92f4.jpg?tbpicau=2024-07-06-05_ce88fc67a07388456cae0d1f118a9c6c)

再继续解 system.img
![](https://tiebapic.baidu.com/forum/pic/item/66c182dea9ec8a13d50636fcaa03918fa1ecc0f9.jpg?tbpicau=2024-07-06-05_0b20203f0749d2d07f8244f7bbeafd42)

/system/app下就是我们熟悉的系统应用了
![](https://tiebapic.baidu.com/forum/pic/item/3d3a022297dda144d85eb661f7b7d0a20ef486f9.jpg?tbpicau=2024-07-06-05_8d1de39564eacd7c9f9035462c0e2df3)

## 贴吧用户_QSANP89

感谢大佬提供的工具和思路，已经实现了系统包解密和再加密，目前只是加密后的第0个byte 原包为00，重生成后的为包大小的数据，目前看原系统包要么是故意改为00，要么出现了错误造成的，车机里的apk读取包大小的时候会读取出异常大小，`((bArr[3] & UByte.MAX_VALUE) << 24) | (bArr[0] & UByte.MAX_VALUE) | ((bArr[1] & UByte.MAX_VALUE) << 8) | ((bArr[2] & UByte.MAX_VALUE) << 16)`，新生成的包已经可以完美解决这个问题了
![](https://tiebapic.baidu.com/forum/pic/item/01a3b61e95cad1c8955bb710393e6709c83d5117.jpg?tbpicau=2024-07-06-05_e7a389b5c203256d9c9557a1a89e74b3)
![](https://tiebapic.baidu.com/forum/pic/item/bb6f2a004a90f6030d53d7707f12b31bb151ed11.jpg?tbpicau=2024-07-06-05_c750fc70627cdbe95836ec0ec4cfa727)
![](https://tiebapic.baidu.com/forum/pic/item/82f11400a18b87d6a9a0e028410828381e30fd12.jpg?tbpicau=2024-07-06-05_0af12239156e40af2dd1d112ac21a777)
![](https://tiebapic.baidu.com/forum/pic/item/b1e78ad9bc3eb1351413fc8ce01ea8d3fc1f441b.jpg?tbpicau=2024-07-06-05_e87118edc289ef6a00bc10c03f9fcd05)

这是成功解密的图
![](https://tiebapic.baidu.com/forum/pic/item/4a1999d062d9f2d3c8c16fd8efec8a136227cc20.jpg?tbpicau=2024-07-06-05_6baf48e3b9cec226eb053e916523122e)
