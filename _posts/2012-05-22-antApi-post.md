---
layout: post
title: "关于ant-pro API 如何发送"
date: 2012-12-11
excerpt: "ant-pro 如何发送给指定的后台 过程的一个简单梳理"
tags: [ant]
comments: true
---

## 前言

其实没用ant-pro 之前 我用过一点VUE 那个时候只知道数据双向绑定，不知到怎么发送数据，
后来用了ant 之后，才发现，原来这么简单。

ant 入手比较难，但是用的时间长了你会发现，它是很方便的。因为它一直遵循组件开发的思想。

<p id = "build"></p>
---

## 正文

*首先找到config 文件下的 config.js文件

* 添加以下代码(其实就是通过正则匹配)
    proxy: {
        '/api/': {
            target: '你要访问的地址',
             changeOrigin: true,
            pathRewrite: { '^/': '' },
         },
     },
     
*然后就可以再api 文件里添加新的api 发送了(我的后台是laravel)
    export async function apiName(params) {
        return request('/url', {
            method: 'POST',
            body: params,
        });
    }


—— L 后记于 2018.11.01


