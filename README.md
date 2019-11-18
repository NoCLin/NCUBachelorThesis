# 南昌大学本科学士学位论文模板（本科毕业设计模板）


由北京邮电大学学士学位论文LaTeX模板[sqyx008/BUPTBachelorThesis](https://github.com/sqyx008/BUPTBachelorThesis) 修改而成，特此表示感谢！

基本按照`南昌大学本科生毕业设计(论文)书写式样`的要求进行了修改。

为简化流程与尽可能保证格式一致性，开题报告等独立文档与论文前封面请使用Word编辑。


## 下载方式
- ```git clone```

## 系统需求

- Windows

    建议直接安装TeX Live（其中已包含需要的XeLaTeX和BibTeX），同时安装TeXworks（安装过程中有勾选框，选中即可）。你也可以使用“TeX Live + 自己喜爱的编辑器 + 扩展”的方式，如使用**TeX Live + Visual Studio Code + LaTeX workshop**或**TeX Live + Atom + language-latex + latex + pdf-view**。
    
    传送门：https://www.tug.org/texlive/

    建议使用TUNA提供的镜像<https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/>进行下载。

- Mac OS 

    建议直接安装MacTeX，编辑器可以使用MacTeX自带的TeXshop，也可以使用TeXpad等其它选择

    传送门：http://www.tug.org/mactex/ 
    
    建议使用TUNA提供的镜像<https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/mac/mactex>进行下载。

    

- Ubuntu Linux

    开源人员尚未在Ubuntu上进行过测试，欢迎尝试并顺利使用本模板的用户在Issue中提交自己的方案

## 如何使用

### 编辑以下文件

- main.tex: 论文的中英文摘要、主体、附录，目前填充的是示例，对照生成的PDF熟悉代码

- bib.ref: 论文的参考文献库


在TeXworks中编译main.tex即可，main.pdf即最终输出。

**注意：如果你在使用中遇到问题，请查看下方FAQ或到Issue板块寻找是否有其它使用者给出的解决方案。**


## 编译

在TeX Live环境下

先用XeLaTeX编译一遍；

再用BibTeX编译一遍；

再用XeLaTeX编译一遍。

（如果里面引用号码没有显示，就再XeLaTeX编译一遍。）

## FAQ

- **Q:LaTeX怎么这么麻烦？**

    A:使用LaTeX排版学术材料是极受欢迎的，优秀的国际会议和权威的学术杂志鲜见不接受LaTeX投稿的，相反，它们会主动提供符合自家排版要求的LaTeX模板，学者不需要再根据其要求大费周折。当然，它对新手不如word友好，因为其不具有“所见即所得”的特性。但是，“信息黄埔”的你们，应该对“看代码→写代码→编译→看结果”这一套十分熟悉，熟练后他会让你不再陷于反反复复调整格式的泥淖。

- **Q:用Word排版有那么不堪么？**

    A:微软的Word是一个优秀的文字处理软件，用它来书写毕业论文没有问题。然而，我们很多同学对它的使用非常肤浅，你甚至还时常能见到“用敲空格的方式把一个标题居中”的人。如果你不太懂自动生成目录，不太懂项目编号，不太懂文档内链接，不太懂上下标，不太懂Word的公式编辑器，不太会调整段落与缩进，不太会处理表格的边框长度和宽度，不太会设置页眉页脚，不太会分节分页，不太会对不同节设置不同页码格式，不太会用合适的方式排列图文……可以说，**你对Word排版的学习成本也是很高的**，既然可以，不妨尝试一种新的排版方式，在撰写学术论文、求职简历和研究生毕业论文时，这项技能还用得上。

- **Q：为什么我在TeXworks中编译，到“Require XeLaTeX”处就不动了？**

    A:正如编译提示所言，它需要XeLaTeX。请注意编辑器左上角是否选择“XeLaTeX”，默认状态下是pdfLaTeX。

- **Q：LaTeX语句书写有误，导致编译卡在一半怎么办？**

    A:TeXworks中，本次编译可以通过在下方输入框敲击Enter以忽略错误完成，但有时错误无法忽略会导致本次输出PDF不成功。修正好错误后，到“文件”中选择“删除辅助文件”，然后再重新编译即可。
    
- **Q：我已经开始写毕设论文了，但该项目的一些样式文件做了更新，怎么办？**

    A:从上面的资料你已经知道需要编辑的文件有哪些，给它们备个份，然后```git pull ```一下，再把备份文件换回；或者直接全盘在另一文件夹编辑你的文档，把更新的配置文件复制过去覆盖即可。
    
- **Q:有一些我需要的排版方式这里没有怎么办？**
    
    A:模板基于LaTeX，你可以随意加入你需要的package，调用你需要的命令。如果你发现你的改动有一定通用性，欢迎修改相应的配置文件提交Pull Request给我；如果你的能力有限，也可以提Issue详述你的改动。合理的Pull Request会被及时merge进master分支，你将在**Contributors**中看到自己，开源项目需要大家共同努力维护。
 
- **Q:引用文献的BibTeX文件可以从哪里获取？**

    A:几乎任何学术文献库都会提供BibTeX格式的引用数据，你可以使用**JabRef**来管理和自动生成你引用文献的BibTeX。但在引用量不大的情况下，直接去学术搜索引擎和数据库（Google Scholar/IEEEXplore/ACM digital library/Springer Link/必应学术/百度学术）或学术组织官网（CVF）去复制也不麻烦。

- **Q:什么样的图片可以插入？**

    A:主流格式如```.png``` ```.jpg```都支持，但如果你将图片保存为```.pdf```格式，会取得更快的编译速度。
    
- **Q:我编译后发现部分引用是问号，怎么办？**

    A:如果是参考文献，确保你已经编译了最新的 ```.bib``` 文件；如果不是，再用XeLaTeX编译一遍。一种粗放的比喻是，**在这里的“编译”就如同Windows的“重启”一样**，虽然暴力但有用。
    

## BTW

再次感谢原项目<https://github.com/sqyx008/BUPTBachelorThesis>。

欢迎提出issue，**关于模板的问题请使用Issue功能提出，其它途径无法得到答复保证**，当然，更欢迎自行解决后提pull request。

如果你愿意，不妨在致谢部分留下**本论文使用基于LaTeX的本科生毕业设计模板书写**，如果你愿意附上本GitHub的链接，那是再好不过了。