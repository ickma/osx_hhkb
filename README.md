####OSX+Jetbrains+HHKB 键盘管理
>使用HHKB，应该尽量避免使用方向键。但对于程序员来说，如果不是纯emacs/vim开发，必须自定义大量的快捷键以避开使用方向键. 在OSX环境下，command键已经被绑定了很多全局快捷键，轻易不要使用，在jetbrains之类的IDE下，control键也默认被绑定了很多快捷键。当然你也可以使用control+option这样的组合键，但是这样的组合不仅按起来麻烦，并且你会发现，这样的组合也已经被绑定了默认快捷键，留给我们可以自定义的键，真的不多。

##### OSX下的option键
option 键默认大量绑定至特殊字符（在英文模式下按option+a/d...等单词就能看到),此时如果直接在JetBrains之类的IDE里直接绑定option+[x]这样的快捷键，虽然能够绑定成功，但是却无法正常使用。所以，为了能够使用option+[x]这样的快捷键，我们首先需要取消OSX默认的对option的绑定。我们使用x_layout这个keyboard kayout来取消系统对option键的默认绑定。

##### x_layout
+ 将x_layout.keylayout 文件放入~/Library/Keyboard\ Layouts路径，并在系统设置-> keyBoard-> Input Sources->other中选择x_layout使之启用
+ x_layout 启用后，会取消原有的controle和option绑定

##### Input Source管理
+ 选择English->ABC输入法,这样在非IDE的环境下使用control+[x]快捷键
+ 选择一个中文输入法
+ 保留x_layout
+ 勾选 Automaticlly switch to a document's inout source,这样可以在切换应用时自动匹配当前应用之前的输入源状态

##### key Binding
+ 为了更好地使用类似emacs的快捷键,绑定option+b/f/d/</>,control+w 6个额外快捷键到全局,分别对应向后删除1个单词/光标前进1个单词/光标后退1个单词/光标跳转到文档开头/光标跳转到文档结尾/向前删除1个单词
+ 将DefaultKeyBinding.dict文件cp到~/Library/KeyBindings路径，重启对应的App，快捷键即时生效.

#### todo
+ [ ] 增加更多实用的emacs键至全局
+ [ ] 修改x_layout ，使它能够恢复系统之前默认绑定的control+[x]风格的emacs快捷键
+ [ ]增加自动部署脚本