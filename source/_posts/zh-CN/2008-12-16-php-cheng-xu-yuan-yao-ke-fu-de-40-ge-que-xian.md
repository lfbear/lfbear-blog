---
layout: post
status: publish
published: true
title: 告别菜鸟 告别这40个迹象
author:
  display_name: 小飞熊
  login: fbbear
  email: fbbear@sina.com
  url: 'https://lfbear.com'
author_login: fbbear
author_email: fbbear@sina.com
author_url: 'https://lfbear.com'
wordpress_id: 56
date: '2008-12-16 17:51:33 +0800'
date_gmt: '2008-12-16 09:51:33 +0800'
categories:
  - 程序人生
tags:
  - php
comments: []
abbrlink: 16717
---
<p>&nbsp;40个迹象表明你还是PHP菜鸟</p>
<p><!--more--></p>
<p>简介<br />
&nbsp;<br />
40个迹象的英文版权归Reinhold Weber所有，中译文作者yangyang。<br />
&nbsp;<br />
正文<br />
&nbsp;<br />
这些迹象并不是为了告诉你还是一个菜鸟，最终是为了告诉你还有很多东西需要学习。<br />
&nbsp;<br />
PHP菜鸟的40个迹象：</p>
<p>&nbsp;<br />
1.不会利用如phpDoc这样的工具来恰当地注释你的代码<br />
&nbsp;<br />
phpDoc是PEAR下的一个优秀模块，如同javadoc一样为代码生成API文档。phpDoc采用OOP的思想编写，它扫描指定目录下的PHP源码，识别出注释中的专用标记然后生成XML文件（或其它），然后建立相应的索引。即本质是从源码中的注释生成文档。<br />
&nbsp;<br />
2.对优秀的集成开发环境如Zend Studio或Eclipse PDT视而不见<br />
&nbsp;<br />
我不知道该怎么描述Zend，只是夜色里有人曾这么说过：PHP界的Zend如同软件界的微软；而Eclipse则是另一款多功能的开发环境，想来大多数人都是用它来写Java的，而PDT即PHP Development Tools则是可以使用户可以在Eclipse写PHP的插件。如果有兴趣，你也可以自己为Eclipse开发个插件。<br />
&nbsp;<br />
&nbsp;<br />
3.从未用过任何形式的版本控制系统，如Subclipse<br />
&nbsp;<br />
版本控制系统？还是先了解一下版本控制吧：版本控制就是数据仓库，它可以记录你对文件的每次更改。这样自然也就了解了什么是版本控制系统了。而进一步的了解不是三两句可以结束的，所以直接推荐，自己选择一个吧！<br />
（1）<a href="http://www.phpchina.com/bbs/thread-43236-1-1.html">http://www.phpchina.com/bbs/thread-43236-1-1.html</a><br />
（2）<a href="http://www.phpchina.com/bbs/thread-46209-1-1.html">http://www.phpchina.com/bbs/thread-46209-1-1.html</a><br />
&nbsp;<br />
&nbsp;<br />
4.不采用某种编码与命名标准，以及通用约定，不能在项目开发周期里贯彻落实<br />
&nbsp;<br />
我觉得良好的代码书写习惯令人很舒服，缩进实在是必需的&mdash;&mdash;要不看着那一堆密密麻麻毫无美感的代码，实在令人郁闷。缩进一般是4个空格，PEAR标准中不建议使用TAB键，因为有些场合会出现问题。而命名建议变量：第一个单词小写开头，其它大写开头如：myName，而类名建议都大写开头如：MyName或者My_Name，至于用不用下划线我觉得差别不大。<br />
&nbsp;<br />
5.不使用统一开发方式<br />
&nbsp;<br />
推荐几篇文章<br />
（1）<a href="http://www.phpchina.com/html/42/1142-7314.html">http://www.phpchina.com/html/42/1142-7314.html</a><br />
（2）<a href="http://www.ibm.com/developerworks/cn/web/wa-jacquard/index.html#N10064">http://www.ibm.com/developerworks/cn/web/wa-jacquard/index.html#N10064</a><br />
&nbsp;<br />
6.不转换（或）也不验证某些输入或SQL查询串（译注：参考PHP相关函数）<br />
&nbsp;<br />
始终坚信一点：绝不相信未经处理的用户输入。而过滤用户输入是Web安全的基础。所以设计者始终应该清楚地知道数据的来源、过滤数据、将已经处理过的数据和未处理的数据区分开。<br />
&nbsp;<br />
7.不在编码之前彻底规划你的程序<br />
&nbsp;<br />
我个人觉得这点和写程序前画流程图之类或者做项目的开发流程一样，应该不需要过多解释。<br />
&nbsp;<br />
8.不使用测试驱动开发<br />
&nbsp;<br />
测试驱动开发（Test Driven Development，英文缩写TDD）是极限编程的一个重要组成部分，它的基本思想就是在开发功能代码之前，先编写测试代码。也就是说在明确要开发某个功能后，首先思考如何对这个功能进行测试，并完成测试代码的编写，然后编写相关的代码满足这些测试用例。然后循环进行添加其他功能，直到完成全部功能的开发。代码整洁可用（clean code that works）是测试驱动开发所追求的目标。<br />
&nbsp;<br />
9.不在错误开启状态下进行编码和测试（译注：参考PHP函数error_reporting）<br />
&nbsp;<br />
我想一般写代码的时候都会开启错误报告吧。这里顺便了解下error_reporting原型为int error_reporting([ int $level])，该函数的作用是设置要显示报告的错误等级，详情参阅：<br />
<a href="http://cn2.php.net/manual/en/function.error-reporting.php">http://cn2.php.net/manual/en/function.error-reporting.php</a><br />
&nbsp;<br />
10.对调试器的好处视而不见<br />
&nbsp;<br />
推荐几款调试器：<br />
（1）Zend IDE<br />
（2）APD<br />
（3）Xdebug<br />
&nbsp;<br />
11.不重构你的代码<br />
&nbsp;<br />
重构是指使用一系列重构准则（手法），在不改变&ldquo;软件之可察行为&rdquo;前提下，调整其结构，是对软件内部结构的一种调整。目的是在不改变&ldquo;软件之可察行为&rdquo;前提下，提高其可理解性，降低其修改成本。重构的好处能改进软件设计使软件更容易被理解，帮助设计者找到BUG，并且提高软件的开发速度。简而言之，重构就是改进已经写好的软件的设计。<br />
&nbsp;<br />
12.不使用类似MVC模式把程序的不同层次划分开<br />
&nbsp;<br />
MVC（Model View Controller）即模型&mdash;视图&mdash;控制器，视图是呈现给用户的一面，模型则是处理任务的模块，而控制器则是控制视图和模型间的映射，即在用户响应下选择何种模型进行处理，而任务处理后控制以何种视图呈现。<br />
&nbsp;<br />
13.不知道这些概念：KISS、DRY、MVC、OOP、REST<br />
&nbsp;<br />
（1）KISS是指Keep It Simple Stupid（摘自wikipedia），指设计时要坚持简约原则，避免不必要的复杂化。<br />
（2）DRY是指Don't Repeat Yourself（摘自wikipedia），特指在程序设计以及计算中避免重复代码，因为这样会降低灵活性、简洁性，并且可能导致代码之间的矛盾。<br />
（3）OOP即Object-Oriented Programming，是指面向对象的程序设计。我一直觉得经典的比喻是汽车是一个类（Class），而这个类的属性有轮子、车身、马达等，方法有加速、减速等；而劳斯莱斯就是一个对象（Object）了，这个对象继承了汽车这个类的属性和方法；而如何实现加速、减速？这样的信息被隐藏了&mdash;&mdash;即信息封装（封装），只留下用户接口给我们了，比如踩刹车、踩油门；至于多态嘛，我粗糙比喻下就是一台自动贩卖机（我们假设它每种价格只有一款饮料），同样是投币这种方法，但是你投进去2元跟5元得到的结果是不一样的&mdash;&mdash;当然，除非这贩卖机有问题。<br />
（4）REST（Representational State Transfer）是一种针对网络应用的设计和开发方式，可以降低开发的复杂性，提高系统的可伸缩性。REST提出了一些设计概念和准则：<br />
a.网络上的所有事物都被抽象为资源（resource）；<br />
b.每个资源对应一个唯一的资源标识（resource identifier）；<br />
c.通过通用的连接器接口（generic connector interface）对资源进行操作；<br />
d.对资源的各种操作不会改变资源标识；<br />
e.所有的操作都是无状态（stateless）。<br />
&nbsp;<br />
14.不用return而是直接在你的函数或类中输出（echo/print）内容<br />
&nbsp;<br />
这一点，观摩大虾的源代码都是用return的，所以我一般也这么学习使用这，至于原因，我就是觉得这样用感觉蛮好的。或许是严禁风格吧。但是其实我对这句有点不理解，函数一般都是需要返回语句的嘛，除非是专门用来输出的函数。<br />
&nbsp;<br />
15.对单元测试或通用测试的优点视而不见<br />
&nbsp;<br />
（1）单元测试是在软件开发过程中要进行的最低级别的测试活动，在单元测试活动中，软件的独立单元将在与程序的其他部分相隔离的情况下进行测试，不仅能保证项目进度还能优化设计。我记得我以前在写比较长的C代码的时候都会在特定模块结束时补一段测试代码来检验，不知道算不算。^_^<br />
（2）通用测试技术？这让我想起图书馆里图灵系列图书的一本《软件测试****》，具体名字忘记了。这些都是属于软件测试的范畴，如果需要可以下载：<br />
<a href="http://bbs.phpchina.com/thread-94241-1-1.html">http://bbs.phpchina.com/thread-94241-1-1.html</a><br />
&nbsp;<br />
16.总是返回硬编码的HTML，却不返回纯粹的数据、字符串或对象<br />
&nbsp;<br />
17.总是对&ldquo;消息&rdquo;和&ldquo;配置参数&rdquo;进行硬编码<br />
&nbsp;<br />
硬编码的使用会造成程序的不灵活，以后修改的复杂问题，还有可能会遇到编译的问题。<br />
^_* 恶补一下：<br />
在计算机程序或文本编辑中，hardcode(这个词比hard code用起来要频繁一些)是指将可变变量用一个固定值来代替的方法。用这种方法编译后，如果以后需要更改此变量就非常困难了。大部分程序语言里，可以将一个固定数值定义为一个标记，然后用这个特殊标记来取代变量名称。当标记名称改变时，变量名不变，这样，当重新编译整个程序时，所有变量都不再是固定值，这样就更容易的实现了改变变量的目的。尽管通过编辑器的查找替换功能也能实现整个变量名称的替换，但也很有可能出现多换或者少换的情况，而在计算机程序中，任何小错误的出现都是不可饶恕的。最好的方法是单独为变量名划分空间，来实现这种变化，就如同前面说的那样，将需要改变的变量名暂时用一个定义好的标记名称来代替就是一种很好的方法。通常情况下，都应该避免使用hardcode方法。　　<br />
有时也用hardcode来形容那些非常难学的语言，比如C或者C++语言，相对的，用softcode来形容象VB这类简单好用的程序语言。<br />
&nbsp;<br />
18.不对SQL查询语句做优化<br />
&nbsp;<br />
SQL语句的优化是将性能低下的SQL语句转换成目的相同的性能优异的<br />
SQL语句。这样的好处是显而易见的，可使用人工智能自动SQL优化。<br />
&nbsp;<br />
19.不使用__autoload（译注：参考PHP手册相关描述）<br />
__autoload函数会在试图使用尚未被定义的类时自动调用。通过调用此函数，脚本引擎在PHP出错失败前有了最后一个机会加载所需的类。<br />
详见：<a href="http://cn.php.net/manual/zh/language.oop5.autoload.php">http://cn.php.net/manual/zh/language.oop5.autoload.php</a><br />
&nbsp;<br />
20.不允许智能错误处理（译注：参考PEAR的ErrorStack）<br />
&nbsp;<br />
PEAR_ErrorStack提供了一种基于堆栈的错误处理方法，将各种错误统一起来指向同一个地方以达到把多个无关项目连接到同一个应用程序的目的。（译自：<a href="http://pear.php.net/package/PEAR_ErrorStack">http://pear.php.net/package/PEAR_ErrorStack</a>）<br />
&nbsp;<br />
21.使用$_GET替代$_POST来做具有破坏性的传递操作<br />
&nbsp;<br />
对于私密的地方，使用$_GET会使一些信息暴露在URL中。<br />
&nbsp;<br />
22.不知道怎么利用正则表达式<br />
&nbsp;<br />
正则表达式？不知道不可怕，来学习吧。<br />
<a href="http://bbs.phpchina.com/thread-89223-1-1.html">http://bbs.phpchina.com/thread-89223-1-1.html</a><br />
&nbsp;<br />
23.从未听说过SQL注入或跨站脚本<br />
&nbsp;<br />
（1）所谓SQL注入，就是通过把SQL命令插入到Web表单递交或输入域名或页面请求的查询字符串，最终达到欺骗服务器执行恶意的SQL命令，比如先前的很多影视网站泄露VIP会员密码大多就是通过Web表单递交查询字符暴出的，这类表单特别容易受到SQL注入式攻击；<br />
（2）业界对跨站攻击的定义如下：&ldquo;跨站攻击是指入侵者在远程Web页面的HTML代码中插入具有恶意目的的数据，用户认为该页面是可信赖的，但是当浏览器下载该页面，嵌入其中的脚本将被解释执行。&rdquo;由于HTML语言允许使用脚本进行简单交互，入侵者便通过技术手段在某个页面里插入一个恶意HTML代码，例如记录论坛保存的用户信息（Cookie），由于Cookie保存了完整的用户名和密码资料，用户就会遭受安全损失。如这句简单的Java脚本就能轻易获取用户信息：alert(document.cookie)，它会弹出一个包含用户信息的消息框。入侵者运用脚本就能把用户信息发送到他们自己的记录页面中，稍做分析便获取了用户的敏感信息。<br />
&nbsp;<br />
24.不允许简易配置，也不允许类的构造函数接受参数传递而后执行set/get方法，或运行时的常量定义<br />
&nbsp;<br />
就一句话：不要不允许类的构造函数接受参数传递。<br />
&nbsp;<br />
25.不理解面向对象编程（OOP）的优势和劣势<br />
&nbsp;<br />
26.不视情形大小而滥用OOP<br />
&nbsp;<br />
27.自认为实现可复用的软件一定等于/需要让你的代码遵循OOP<br />
&nbsp;<br />
OOP的优点：使人们的编程与实际的世界更加接近，所有的对象被赋予属性和方法，结果编程就更加富有人性化。OOP的缺点：就C++而言，由于面向更高的逻辑抽象层，使得C++在实现的时候，不得不做出性能上面的牺牲，有时候甚至是致命的。<br />
&nbsp;<br />
28.不利用智能缺省值<br />
&nbsp;<br />
我想，使用缺省值是个好习惯。<br />
&nbsp;<br />
29.没有单一的配置文件<br />
&nbsp;<br />
专门设置个config.php我想是需要的。<br />
&nbsp;<br />
30.不想暴露文件源码，却用.inc后缀名取代了.php<br />
&nbsp;<br />
*.inc文件顾名思义是include file的意思，一般我们使用inc作为后缀，是因为这样能体现该文件的作用。*.inc文件的作用有点类似于C/C++内的*.H、*.HPP头文件，使用inc文件可以使我们的程序，增加可读性，更易于开发和维护。<br />
&nbsp;<br />
31.不使用数据库抽象层<br />
&nbsp;<br />
请参考<a href="http://bbs.phpchina.com/thread-94258-1-1.html">http://bbs.phpchina.com/thread-94258-1-1.html</a><br />
&nbsp;<br />
32.不能保持DRY（请参考13点）作风，即不重复自己，如果你总是在复制粘贴一些东西，说明你设计得很差劲<br />
&nbsp;<br />
33.没有实现让一个函数/类/方法只做一件事，也不能组合利用它们<br />
这需要锻炼，在实践中学习、完善着。<br />
&nbsp;<br />
34.没能尝试OOP的特长，如抽象类、接口、多态、继承，访问控制修饰符（译注：如public、private、protected）<br />
&nbsp;<br />
哦，mygod，我想还是参考25-27点吧，也是需要在实践中成长的。<br />
&nbsp;<br />
35.不用现有的设计模式优化你的程序体系设计<br />
&nbsp;<br />
推荐《HeadFirst》设计模式<br />
&nbsp;<br />
36.不允许你的用户在你拥有很多文件或目录的情况下定义基础目录<br />
&nbsp;<br />
程序一旦上线可能会产生很多log文件或者在后期升级程序的时候会把文件或目录搞得很乱。一个好的建议是将所有路径定义到一个文件中，允许你的用户（开发者）来更改这些，以便系统有一个良好的结构。<br />
&nbsp;<br />
37.污染了名称空间，比如用常见字符串命名你的库函数<br />
&nbsp;<br />
哎，这实在是个不好的习惯，不过好习惯是养成的！<br />
&nbsp;<br />
38.使用数据库表时不使用表前缀<br />
&nbsp;<br />
我想，可能，PHPChina的数据表的前缀是PPC_或者PCC_。这的确是有好处的，我觉得，就好像字段名使用如txtUsername这样的格式。<br />
&nbsp;<br />
39.不使用统一的模板引擎<br />
&nbsp;<br />
我想谁都不想让自己的系统页面很慢的出现在用户的浏览器上吧，一个团队一般都使用统一的模板引擎。<br />
&nbsp;<br />
40.不关注已有的PHP开发框架，懒于探索；其实先进的开发理念和美妙代码就蕴含其中。<br />
比如Zend Framework、CakePHP、FleaPHP、ThinkPHP等。<br />
&nbsp;<br />
整理自网络，感谢作者和译者的努力！</p>
