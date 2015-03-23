# 用于ucore_lab的qemu(with DECAF)
## 编译运行

1. 编译decaf
```
cd decaf_googlecode
./configure --target-list=i386-softmmu --enable-vmi --enable-tcg-taint
make
```

2.编译ucore lab
```
git clone https://github.com/chyyuu/ucore_lab
cd ucore_lab/labcodes/lab1
make   
```

3.编译插件func_log, func_log插件默认路径是plugins/func_log
```
cd decaf_googlecode/plugins/func_log
./configure --decaf-path=[decaf_googlecode root path]  --lab-path=[ucore lab root path]
// build plugin: func_log
make
// analysis ucore lab
make qemu
```

<Syracuse System Security (Sycure) Lab>

Welcome to DECAF, release 1.0.

DECAF(Dynamic Executable Code Analysis Framework) is the successor to 
the binary analysis techniques developed for TEMU(dynamic analysis component
of BitBlaze) as part of Heng Yin's work on BitBlaze project headed up by Dawn Song.
DECAF builds upon TEMU. We appreciate all that worked with us on that project.

For copyright information see the COPYING_DECAF file.
for installation instruction see INSTALL file.

For more information about DECAF and other softwares, see our
web site at:
http://sycurelab.ecs.syr.edu/

If you have any questions about DECAF,please post it on 
http://code.google.com/p/decaf-platform/

