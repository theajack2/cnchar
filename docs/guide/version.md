
## 1.0（基础版本）
1. 获取 **汉字拼音** ，支持首字母、大小写、数组分割
2. 获取 **汉字笔画数**

## 2.0 （升级版本）
1. 备选 **多音字** 等功能
2. 支持 **多音词**
3. 支持 **拼音音调**
4. 获取汉字 **笔画顺序** 、笔画详细名称、通过笔画顺序推出原汉字等
5. 支持 **简体字** 、 **繁体字** 、 **火星文** 互转
6. 支持 **繁体字** 拼音、笔画数，实现和简体字一样的功能
7. **体积小**，最小压缩版本仅 42 kb
8.  **多端可用**，可用于 原生浏览器环境、webpack环境、nodejs环境...，几乎支持所有js能运行的环境
9.  丰富的配置，按需取用

## 2.0.2
1. 添加多音字默认读音字典
2. 增加根据笔画数反推导出汉字的功能 orderToWord
3. 修改一些多音字的默认读音

## 2.0.3
1. 去除 origin 参数，多音词模式下使用 poly参数会启用备选多音字功能而禁用多音词功能
2. orderToWord 加入繁体字支持，参数修改为 ['all','simple']
3. 增加参数校验中提示可选值
4. 对词库进行一些修改

## 2.0.4
1. 主要扩充了繁体字库
2. 修改了 繁体字、简体字、火星体之间的转换方法，只保留了六个转换方法

## 2.0.5 - 2.0.6
1. 加入了 typescript 声明文件 index.d.ts
2. script 方式引用增加了 latest.min.js 版本

## 2.0.7
1. 加入 eslint 和 commitlint
2. 使用 gulp-babel 转换源代码到 npm 包，使得即便禁用了对node_module的babel转换，也可以正常使用cnchr
3. 修复了多音字广和厂的默认读音

## 2.0.8
1. 扩充了217个词频高于100的汉字
2. 修改orderToWord.orders 笔画名称的显示，如果某个笔画有两个现在会保留两个名称
3. orderToWord 笔画数组支持使用空格分隔的笔画字符串
3. orderToWord 默认返回字符串 如需返回数组请加上 array 参数
4. orderToWord 修改all参数为start 增加 contain、match、matchorder参数，优先级 match>matchorder>contain>start>默认
5. 加入 cnchar.spellToWord 方法
6. 加入 cnchar.strokeToWord 方法
7. 加入 cnchar.spellInfo 方法，spellInfo.tones spellInfo.initials属性
8. 仓库加入测试目录

## 2.0.9
1. 修复 多音词"致远任重" 中的 重 字拼音错误
2. 增加 齉 字 [nàng 36]
3. 无字默认读音修正
4. 修改 13 个多音字的默认读音
5. 增加 15 个多音词

## 2.1.0
1. 增加cnchar-draw插件，支持可视化绘制汉字笔画，多种模式可选
2. 将cdn移至npm包中，改变cdn引用方式，删除dist目录
3. 使用vuepress构建文档，工程化重构文档
4. 使用gulp-markdown-toc

## 2.1.1
1. 修复cnchar-all依赖的bug

## 2.1.2
1. 增加draw背景色设置
2. 修正几个多音词
3. 统一 trad 和 simple 参数
4. 移除了一字和三字的繁体（应该是大写不是繁体）
   
## 2.1.3
1. draw库增加clear参数，表示绘制前是否清空容器
2. draw库将backgroundColor参数默认值改为#fff
3. draw库将el参数改为支持css选择器或dom