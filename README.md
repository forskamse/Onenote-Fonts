# onenote_font
中文环境下，OneNote中输入中文会被强制为宋体，输入英语时变为Calibri，很不舒服。
可以用微软雅黑来替代（其他字体当然亦可，全凭喜好），无论输入中英文都统一为微软雅黑，操作如下：
## 修改字体设置
- 进入C:\Windows\Fonts\Calibri，右键“Calibri常规-属性-安全-高级”里将所有者从“TrustedInstaller”改为“Users”（直接输入即可），然后在编辑里将Users的完全控制选上；
- 打开E:\File\OneNote\Fonts\OneNote.ttf文件安装替换Calibri字体即可。
<div align=center>
![1](1.jpg)
![2](2.jpg)
![3](3.jpg)
![4](4.jpg)
![5](5.jpg)
</div>
## 提取修改字体
提取微软雅黑字体，并修改成伪Calibri字体。（仓库中给出操作后的文件，具体流程附后）
msyh_0.ttf、msyh_1.ttf为微软雅黑字体提取文件，OneNote.ttf为最终字体文件，OneNote.fcp是FontCreator工程文件。
## 安装并替换字体
双击OneNote.ttf安装Calibri字体即可（提示是否替换时选择“是”）

## 原始来源
[OneNote英文字体自动变成Calibri的问题有没有什么解决办法？](https://www.zhihu.com/question/30089364/answer/235971324)

win10下的终极版解决方案：

1、进入C:\Windows\Fonts找到Calibri字体，点进去后先右键”Calibri常规-属性-安全-高级”里将所有者从“TrustedInstaller”改为“Users”（直接输入即可），然后在编辑里将Users的完全控制选上。（修改前删除的话会提醒是受保护的系统字体，修改后只会提醒它正在使用，或者有时候就能成功删除）

2、下载FontCreator（FontCreator9.0绿色汉化特别版-找字网,您的字体管家!免费字体下载,字体设计!），打开，文件-打开已安装字体，选择微软雅黑Regular（或Microsoft YaHei UI），将ttc文件提取为两个ttf文件，之后把任意一个拖入软件窗口内，开始修改：

3、进入字体-属性-标识符，先将字系改为Calibri，然后进入自定义，将里面内容全删。之后文件-输出字体-TrueType，后缀.ttf保存

4、点开字体文件，安装，替换，ok。（如果不行，把Calibri常规删掉再安装一次就好了）
