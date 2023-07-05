# hash4cmd
在win xp+ 环境中不使用其他插件的情况下，对文件目录下的文件（含子文件夹的文件，不含隐藏文件）进行hash，可重复执行查看文件hash是否发生变化。

## 功能
 - 对文件目录下的文件（含子文件夹的文件，不含隐藏文件）进行hash；
 - 生成文件：文件名包含hash部分摘要，文件内包含完整hash结果、文件基本信息；
 - 重新运行命令生成log，记录hash发生变化的文件，记录新增加的文件；

## 特点
 - 本质上为使用`certutil -hashfile`命令，故可在win xp+（或win 2003+）环境下使用；
 - 使用`for /r`遍历文件夹，相对于`dir /ad /b /s`更快，但也会遗漏隐藏文件；
 - 由于Batch的延迟变量特性，会出现各种各样意想不到的问题 :) 。
