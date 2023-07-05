hash2cmd：在仅存在certutil.exe的情况下对文件目录下的文件（含子文件夹的文件，不含隐藏文件）进行hash，可重复执行查看文件hash是否发生变化。

功能：
    1、对文件目录下的文件（含子文件夹的文件，不含隐藏文件）进行hash；
    2、生成文件：文件名包含hash部分摘要，文件内包含完整hash结果、文件基本信息；
    3、重新运行命令生成log文件，记录hash发生变化的文件，记录新增加的文件；

特点：
    1、本质上使用certutil -hashfile命令，故可在win 7+环境下使用；
    2、使用for /r遍历文件夹，相对于dir /ad /b /s更快，但也会遗漏隐藏文件；
    3、由于batch的延迟变量特性，会出现各种各样意想不到的问题:)。

许可：
   MIT License
      
