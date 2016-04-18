# 简介





## 安装

* 需要安装`ctags`、`cscope`程序.

如果是Linux系统，运行如下命令进行安装：

    $ git clone https://github.com/wangleihd/software.git
    $ cd software
    $ ./install.sh

## 使用
 * 按[`,f`]打开右边文件浏览器窗口。 再按一下 [`,f`] 关闭这个窗口。
 * 按[`,e`]并输入你想打开的文件的名字（可以使用正则表达式）再按Tab进行选择，回车就可以打开。
 * 按[`,t`]将会在Vim的左边打开一个Taglist窗口。 再按一下 [`,t`] 关闭这个窗口。
 * 按[`Ctrl+]`]就会跳到宏的定义处，按[`Ctrl+o`]就会跳回来。 [`:help tagsrch.txt`]查看帮助文档。
 * cscope也可以用来在代码间跳来跳去，但有些功能是ctags所没有的，比如查找某个函数被哪些函数调用
    过、查找某个文件被哪些文件引用过等等，在.vimrc里面定义了使用cscope的快捷键，比如将光标放在
    某个函数上使用命令",sc"就可以查看这个函数被哪些函数调用过，使用命令",sg"就可以跳转到函数的
    定义处。更多的使用方法请使用命令":help if_cscop.txt"查看帮助文档。

*   如果你想调试，你得先安装gdb。在Gvim下有插件完美支持Vim下的gdb调试，但终端下的Vim只有当Vim
    编译的时候打了vimgdb的补丁才能用gdb来调试。如果你的Vim在编译的时候打了此补丁，你可以通过
    <F7>来调试。详细的调试命令请使用":help vimgdb"打开帮助文档。

*   现在你可能打开了很多个文件，如果你想查看当前打开了哪些文件，可以使用命令",be"在当前窗口中
    打开buffer浏览器，上下选择文件回车就可以打开。更多的使用方法请使用":help bufexplorer.txt"
    查看帮助文档。

*   打开一个C文件，输入几个字符，除非你运气实在不好，否则你就会看到一个弹出菜单。里面会根据你
    输入的内容提示补全。用上下或"Ctrl-p","Ctrl-n"进行选择。在结构体变量后输入"."或"->"的时候
    也会根据结构成员补全。更多的使用方法请使用":help acp.txt"和":help omnicppcomplete.txt"
    查看帮助文档。

*   打开一个C文件，在一个函数实现体中调用另外一个函数。当你输入完这个被调用的函数名，在输入左括
    号的时候在Vim的下方就会显示函数的原型。详细帮助文档请参考echofunc插件。

*   打开一个文件，在一行的开头输入main再按"Tab"键试试，main函数就这样出来了，在main函数里面输入
    for再按几个"Tab"看看会出现什么效果。更多的代码自动完成请查看文件
    "vimfiles/bundle/snipMate/snippets/c.snippets"，当然你也可以自己定义代码自动完成，定义方法
    请使用":help snipMate.txt"，请在vimrc里面修改自己的个人信息
    g:snip_author,g:snip_mail,g:snip_company.

