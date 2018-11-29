    questam10.2b linux64 位如何安装到 ubuntu 14.0.4lts上

1.基本的安装思路与在rhel上安装没有区别，具体思路可参见以前总结的文档2015年的

2.安装过程中遇到的问题及解决方法

    2.1问题1, 执行./install.linux时候，无法弹出界面，解决方法
    解决方法：sudo apt-get install libXtst6:i386 
    执行该命令即可

    2.2问题2，破解过程中执行./patch_2010时候，报错
    错误名称：./sfk: error while loading shared libraries: libstdc++.so.5: wrong ELF class: ELFCLASS64
    附加：patch_2010的路径：/opt/tool/mentor/questasim10_2b/questasim/linux_x86_64/mgls/lib
    解决方法：将以前rhel5.6上面的libstdc++.so.5xx 文件放到/usr/lib下面即可
              这个文件就在当前目录下，如果不行，可以尝试libxxx下面的其他文件,试试放在/usr/lib64下面                                                                        
3.如果很多库都丢失，终极解决方法，就是在界面情况下，点击ia32-libs_2016.02.18_amd64.deb，这个文件，网上更新 安装32位的库                                                                    
 
