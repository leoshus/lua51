README for Lua 5.1

See INSTALL for installation instructions.
See HISTORY for a summary of changes since the last released version.

* What is Lua?
  ------------
  Lua is a powerful, light-weight programming language designed for extending
  applications. Lua is also frequently used as a general-purpose, stand-alone
  language. Lua is free software.

  For complete information, visit Lua's web site at http://www.lua.org/ .
  For an executive summary, see http://www.lua.org/about.html .

  Lua has been used in many different projects around the world.
  For a short list, see http://www.lua.org/uses.html .

* Availability
  ------------
  Lua is freely available for both academic and commercial purposes.
  See COPYRIGHT and http://www.lua.org/license.html for details.
  Lua can be downloaded at http://www.lua.org/download.html .

* Installation
  ------------
  Lua is implemented in pure ANSI C, and compiles unmodified in all known
  platforms that have an ANSI C compiler. In most Unix-like platforms, simply
  do "make" with a suitable target. See INSTALL for detailed instructions.

* Origin
  ------
  Lua is developed at Lua.org, a laboratory of the Department of Computer
  Science of PUC-Rio (the Pontifical Catholic University of Rio de Janeiro
  in Brazil).
  For more information about the authors, see http://www.lua.org/authors.html .

(end of README)

###虚拟机运转核心功能

|文件名|描述|
|---|---|
|lapi.c  |C语言接口|
|lctype.c |C 标准库中ctype相关实现|
|ldebug.c|Debug接口|
|ldo.c|函数调用以及栈管理|
|lfunc.c|函数原型及闭包管理|
|lgc.c|垃圾回收|
|lmem.c|内存管理接口|
|lobject.c|对象操作的一些函数|
|lopcodes.c|虚拟机的字节码定义|
|lstate.c|全局状态机|
|lstring.c|字符串池|
|ltable.c|表类型的相关操作|
|ltm.c|元方法|
|lvm.c|虚拟机|
|lzio.c|输入流接口|

###源代码解析以及预编译字节码

|文件名|描述|
|---|---|
|lcode.c|代码生成器|
|ldump.c|序列化预编译的lua字节码|
|llex.c|词法分析器|
|lparser.c|解析器|
|lundump.c|还原预编译的字节码|

###内嵌库

|文件名|描述|
|---|---|
|lauxlib.c|库编写用到的辅助函数库|
|lbaselib.c|基础库|
|lbitlib.c|位操作库|
|lcorolib.c|协程库|
|ldblib.c|Debug库|
|linit.c|内嵌库的初始化|
|liolib.c|IO库|
|lmathlib.c|数学库|
|loadlib.c|动态扩展库管理|
|loslib.c|OS库|
|lstrlib.h|字符串库|
|ltablib.c|表处理库|

###可执行的解析器、字节码编译器

|文件名|描述|
|---|---|
|lua.c|解释器|
|luac.c|字节码编译器|
