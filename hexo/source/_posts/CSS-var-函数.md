---
title: CSS var() 函数
date: 2020-03-02 09:02:04
tags: css
catrgories: css
---

# CSS var() 函数 [官方说明](https://www.runoob.com/cssref/func-var.html)

> 定义一个名为 "--main-bg-color" 的属性，然后使用 var() 函数调用该属性：

    :root {
    --main-bg-color: coral;
    }
    
    #div1 {
    background-color: var(--main-bg-color);
    }
    
    #div2 {
    background-color: var(--main-bg-color);
    }

## 定义与用法
var() 函数用于插入自定义的属性值，如果一个属性值在多处被使用，该方法就很有用。支持版本：CSS3

## CSS 语法
    var(custom-property-name, value)

|值|描述|
|--|--|
|custom-property-name|必需。自定义属性的名称，必需以 \-\- 开头。|
|value|可选。备用值，在属性不存在的时候使用。|

<font color=red>可以理解为带语法的全局变量</font>

## 更多实例

    :root {
    --main-bg-color: coral;
    --main-txt-color: blue;
    --main-padding: 15px;
    }
    
    #div1 {
    background-color: var(--main-bg-color);
    color: var(--main-txt-color);
    padding: var(--main-padding);
    }
    
    #div2 {
    background-color: var(--main-bg-color);
    color: var(--main-txt-color);
    padding: var(--main-padding);
    }

