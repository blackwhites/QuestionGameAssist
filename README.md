# QuestionGameAssist
**百万英雄、芝士超人、冲顶大会、百万赢家自动答题助手，基于之前的开源版本做了很多优化，这可能是最全网最快，结果最清晰的版本。**

**可以在 3 秒左右运行完，扫视完结果后还有时间参考其他助手（搜狗搜索）再作出判断答题。P.S. 搜狗搜索时常有出错的情况，多个工具多个参考**

**原理：** 实时截取屏幕，选取问题区域判断是否有答题框，有则判断问题是否有更新（答题框上1/3区域的二值图求diff），有更新则调用百度的ocr提取出问题和选项拼接后调用搜狗搜索，并解析结果对问题和选项关键字分别用红色和黄色高亮加粗显示。

## 运行界面
![运行界面](https://github.com/wenmin-wu/QuestionGameAssist/blob/master/interface.png?raw=true)

## 使用说明
**用的是Python3.5**
1,安装ADB 驱动，可以到[这里下载](https://adb.clockworkmod.com/)<br />
   安装 ADB 后，请在环境变量里将 adb 的安装路径保存到 PATH 变量里，确保 adb 命令可以被识别到
  
2.需要安装模块 在命令行输入(pip install 模块名称) 模块名称： baidu-aip  lxml opencv-python bs4

3.在assist.py里填写自己百度ocr的APPid</br>
百度ocr：http://ai.baidu.com/tech/ocr/general

4.连接手机<br>在答题前运行python3 assist.py 后面全程自动 :)

## 参考项目
* https://github.com/wuditken/MillionHeroes
