## --input 和 -i
在python中的定义时决定的。args接受("-i","--input",type=str/int,help="作为输入"可以再有defaut) <br>
由于这个是用户自己定义的，那么有时候如果不提供-- ,- 的时候，也就会没有这两个选项，并不奇怪。但是建议加上--和-来让命令和参数保持一定的区分度。以及，对于复杂的参数输入，我们最好可以做成config.json然后读取。 <br>

## #!/bin/bash 的作用

#!/bin/bash 是一个特殊的注释行，通常出现在 Bash shell 脚本文件的第一行。这一行被称为"shebang"或"hashbang"，它的作用是告诉操作系统要使用哪个解释器来执行该脚本。 <br>

## if fi
if [ 条件判断 ]; then <br>
  #条件为真时执行的命令 <br>
fi <br>

-le 表示 "less than or equal to"（小于等于）。<br>
-ge 表示 "greater than or equal to"（大于等于）。<br>

if [ ${stage} -le 1 ] && [ ${stop_stage} -ge 1 ]; then <br>
  #某些命令 <br>
fi <br>

