gdb 调试的过程中无法读取STL容器中的数据

可以将这个文件放到任意一个目录下

gdb a.out
之后 进入gdb调试页面
source stl-views-1.0.3.gdb (绝对路径)

也可以可以下载这个文件，下载后把它放到用户目录下改名为.gdbinit。之后再进入 gdb就可以用以下这些命令查看容器内容了：
pvector, plist, pmap, pset, pdequeue, pstack, pqueue, ppqueue, pbitset, pstring, pwstring
用help可以查看命令的帮助，比如help pvector。这个方法可以支持广泛的gdb 版本，据说是GDB 4.3+都可以。

使用多态时候使用ptype指令 查看基类指针类型 只能看到基类的类型 如果要看到基类指针真实指向的子类类型需要设置
set print object on
