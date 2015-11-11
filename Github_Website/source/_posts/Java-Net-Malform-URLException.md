title: 解决java.net.MalformedURLException_unknown protocol_c问题
date: 2015-11-12 06:07:10
categories: 日常积累
tags: 
- Java
- Exception

thumbnail: http://chearty.xyz/images/JavaNetURLException.jpg
banner: http://chearty.xyz/images/JavaNetURLException.jpg

---

最近在工作中遇到的问题，困扰了很长时间。

<!--more-->


----------


- 修改前代码：

    DocumentBuilderFactory factory = DocumentBuilderFactory.newInstance();
    
    DocumentBuilder builder = factory.newDocumentBuilder();
    
    Document document = builder.parse(xmlPath);  \\直接将路径名给builder.
	


----------

- 修改后代码：

    DocumentBuilderFactory factory = DocumentBuilderFactory.newInstance();
    
    DocumentBuilder builder = factory.newDocumentBuilder();
    
    Document document = builder.parse("file:///" + xmlPath);