# LearningNote
个人学习笔记

## 阅读环境配置
1. 配置Latex + VsCode
- 下载[TexLive2022](https://mirrors.huaweicloud.com/CTAN/systems/texlive/Images/)
- 下载[VsCode](https://code.visualstudio.com/#alt-downloads)
- 下载[git](https://git-scm.com/)
- 下载Tex插件LaTex Workshop
VsCode 左侧出现tex插件按钮，可用于构建项目；也可以直接点击右上角的绿色箭头构建项目。
2. 在云端新建项目并初始化项目环境
- 在github中新建repository，如命名为LearningNote，其中*Add gitignore* 选择添加TeX以防止将LaTex编译过程中的缓存文件上传到云端。
- 可选择性的添加README文件。
3. 下载笔记项目并添加笔记模板
- 若本地不存在项目：
```bash
git clone https://github.com/username/LearningNote
git submodule add https://github.com/Azure1210/elegantbook-magic-revision.git
```
- 若本地存在项目：
```bash
git pull
```
4. 编辑Latex模板
- 在文件夹LearningNote下新建笔记文件夹，如命名为Note，存放资源文件
- 拷贝模板文件夹中的figure到自定义的笔记文件夹Note目录下
- 修改模板中的路径为相对路径，导入Latex格式
```tex
\documentclass[lang=cn,10pt]{../elegantbook-magic-revision/elegentbook-magic-revision/gorgeousnbook}
```
- 参考模板 *gorgeousnbook-cn.tex* 编写文档，项目结构如下:
``` tree
-LearningNote

--elegantbook-magic-revision

--Note_1
----figure/*.jpg
----chap_a/*.tex
----chap_b/*.tex
----Note_1.tex

--Note_2
----figure/*.jpg
----chap_a/*.tex
----chap_b/*.tex
----Note_2.tex
```  
每个笔记本的总体框架放在笔记本的第一层子目录下，而笔记本锁对应的每个具体的章节放在第二层的子目录下。
5. 上传本地文档到云端
```bash
git add .
git commit -m "commit information"
git push
```
6. 多机编辑与阅读
- 下载github的项目
```bash
git clone https://github.com/username/LearningNote.git --recurse-submodules
```
- 编辑Tex源码，产生PDF文件并阅读
- 上传新的Tex源码
```
git pull
```

感谢Latex模板[elegantbook-magic-revision](https://github.com/Azure1210/elegantbook-magic-revision)。

## 笔记内容
### **STLRLResearch**