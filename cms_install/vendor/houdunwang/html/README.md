# 生成静态

##介绍 
生成静态 html 好处很明显，第一点是非常有利于 SEO 的优化，搜索引擎可以对 html文件进行更好的收录。第二点是显著减轻网站的负载，WEB 服务器在处理 html 文件时只是简单的读取操作，不会经由 PHP 模块进行处理，也不会有数据库服务器的操作，所以速度要较 PHP 文件快得多。 

HTML 有很多特点，但是我们也不能盲目使用 HTML，而是应该在更新频率较低的页面采用 HTML 处理方式 ，比如说文章系统、博客系统，社区门户等方面，而在更新频率较高的应用如论坛、微薄、SNS 等方面建议采用  

[TOC]

#开始使用
####参数说明
```
Html::make(动作,GET参数,静态文件)
动作: [类,方法]
参数: 数组类型系统将保存到GET中供方法使用
文件: 生成的静态文件
```

####生成静态
```
$data = [
    ['id' => 1],
    ['id' => 2],
    ['id' => 3],
];
foreach ($data as $d) {
    Html::make([App::class, 'show'], $d, "html/{$d['id']}.html");
}
```





