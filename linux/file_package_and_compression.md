## File Package and Compress ##
### Common Package Format and Tools ###
| File Suffix  | Discription |
| :------------- | :------------- |
|*.zip	|zip 程序打包压缩的文件|
|*.rar	|rar 程序压缩的文件               
|*.7z   	|7zip 程序压缩的文件
|*.tar	  |tar 程序打包，未压缩的文件
|*.gz	   | gzip 程序（GNU zip）压缩的文件
|*.xz	   | xz 程序压缩的文件
|*.bz2	  |bzip2 程序压缩的文件
|*.tar.gz|	tar 打包，gzip 程序压缩的文件
|*.tar.xz|	tar 打包，xz 程序压缩的文件
|*tar.bz2|	tar 打包，bzip2 程序压缩的文件
|*.tar.7z|	tar 打包，7z 程序压缩的文件    

### tar ###
```tar``` is the most commonly used package and compress command in Linux, and it also provides support for ```gz, xz, b2z```

* ```-c``` create a .tar File
* ```-f``` specify a file name for tar file, the file name should be right behind this parameter
* ```-x``` to unpackage a .tar file
* ```-t``` view the content of tar file without unpackage it.

### tar with other format ###
| compress format | parameter |
| :------------- | :------------- |
| *.tar.gz       | -z |
| *.tar.xz       | -J |
| *.tar.bz2      | -j |

### Summary ###
* zip：

  - 打包 ：```zip something.zip something``` （目录请加 -r 参数）

  - 解包：```unzip something```
  - 指定路径：-d 参数

* tar：

  - 打包：```tar -zcvf something.tar something```
  - 解包：```tar -zxvf something.tar```
  - 指定路径：-C 参数
