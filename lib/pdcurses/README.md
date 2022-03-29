# 编译说明

## win

> 参考资料  
> [https://blog.csdn.net/sinat_29235897/article/details/92850542](https://blog.csdn.net/sinat_29235897/article/details/92850542)  
> [https://www.cnblogs.com/yapingxin/p/15936414.html](https://www.cnblogs.com/yapingxin/p/15936414.html)  

- 在 `PDCurses\wincon\Makefile.vc` 的15行之后添加一个变量
  ```
  PLATFORM = X64
  ```
- 编译命令
  ```powershell
  # DEBUG 版本
  nmake -f Makefile.vc WIDE=Y UTF8=Y DLL=Y DEBUG=Y

  # RELEASE 版本
  nmake -f Makefile.vc WIDE=Y UTF8=Y DLL=Y
  ```
  - 说明
    - `WIDE=Y` 开启宽字符支持
    - `UTF8=Y` 设置为 UTF-8 编码
    - `DLL=Y` 编译 DLL 文件
    - `DEBUG=Y` 是否 DEBUG 版本