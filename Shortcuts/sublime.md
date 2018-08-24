**Ctrl+Shift+P**（菜单 – Tools – Command Paletter），输入 install 选中Install Package并回车

Ctrl+Shift+P：打开命令面板
Ctrl+P：搜索项目中的文件
Ctrl+G：跳转到第几行
Ctrl+W：关闭当前打开文件
Ctrl+Shift+W：关闭所有打开文件
Ctrl+Shift+V：粘贴并格式化
Ctrl+D：选择单词，重复可增加选择下一个相同的单词
Ctrl+L：选择行，重复可依次增加选择下一行
Ctrl+Shift+L：选择多行
Ctrl+Shift+Enter：在当前行前插入新行
Ctrl+X：删除当前行
Ctrl+M：跳转到对应括号
Ctrl+U：软撤销，撤销光标位置
Ctrl+J：选择标签内容
Ctrl+F：查找内容
Ctrl+Shift+F：查找并替换
Ctrl+H：替换
Ctrl+R：前往 method
Ctrl+N：新建窗口
Ctrl+K+B：开关侧栏
Ctrl+Shift+M：选中当前括号内容，重复可选着括号本身
Ctrl+F2：设置/删除标记
Ctrl+/：注释当前行
Ctrl+Shift+/：当前位置插入注释
Ctrl+Alt+/：块注释，并Focus到首行，写注释说明用的
Ctrl+Shift+A：选择当前标签前后，修改标签用的
F11：全屏
Shift+F11：全屏免打扰模式，只编辑当前文件
Alt+F3：选择所有相同的词
Alt+.：闭合标签
Alt+Shift+数字：分屏显示
Alt+数字：切换打开第N个文件
Shift+右键拖动：光标多不，用来更改或插入列内容
Ctrl+依次左键点击或选取，可需要编辑的多个位置
Ctrl+Shift+上下键：替换行

 



- **Alignment**
  代码对齐，如写几个变量，选中这几行，Ctrl+Alt+A，哇，齐了。

- **Prefixr**写 CSS可自动添加 -webkit 等私有词缀，Ctrl+Alt+X触发。

- Emmet html/CSS快速编辑（原名Zen Coding）
  Zen Coding估计大家都不会陌生，前不久改名为Emmet了，虽然用Emmet编辑html很快，但是要用好用快它需要付出不小的学习成本，

- SublimeTmpl 快速生成文件模板
  SublimeTmpl 能新建 html、css、javascript、php、python、ruby 六种类型的文件模板，所有的文件模板都在插件目录的templates文件夹里，可以自定义编辑文件模板。
  SublimeTmpl默认的快捷键
  ctrl+alt+h → html
  ctrl+alt+j → javascript
  ctrl+alt+c → css
  ctrl+alt+p → php
  ctrl+alt+r → ruby
  ctrl+alt+shift+p → python
  如果想要新建其他类型的文件模板的话，先自定义文件模板方在 templates 文件夹里，再分别打开 Default (Windows).sublime-keymap、Default.sublime-commands、Main.sublime-menu、SublimeTmpl.sublime-settings 这四个文件照着里面的格式自定义想要新建的类型~

- TrailingSpacer 高亮显示多余的空格和 Tab
  我有代码洁癖，我爱 TrailingSpacer，TrailingSpacer这款插件能高亮显示多余的空格和Tab，并可以一键删除它们。

  注意，在 github 上下载的插件缺少了一个设置快捷键的文件，可以新建一个名字和后缀为 Default (Windows).sublime-keymap 的文件，添加以下代码，即可设置“删除多余空格”和“是否开启TrailingSpacer ”的快捷键。

```
[
    { "keys": ["ctrl+alt+d"], "command": "delete_trailing_spaces" },
 
    { "keys": ["ctrl+alt+o"], "command": "toggle_trailing_spaces" }
]
```

- CSScomb CSS属性排序
CSScomb 可以按照一定的 CSS 属性排序规则，将杂乱无章的 CSS 属性进行重新排序。选中要排序的 CSS 代码，按 Ctrl+Shift+C，即可对 CSS 属性重新排序了，代码从此简洁有序易维护，如果不款选代码则插件将排序文件中所有的 CSS 属性。当然，可以自己自定义 CSS 属性排序规则，打开插件目录里的 CSScomb.sublime-settings 文件，更改里面的 CSS 属性顺序就行了。因为这个插件使用 PHP 写的，要使他工作需要在环境变量中添加 PHP 的路径，具体请看 github 上的说明。