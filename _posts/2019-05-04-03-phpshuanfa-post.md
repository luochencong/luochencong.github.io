---
layout: post
title: "php排序算法"
date: 2019-04-03
excerpt: "基础排序算法"
tags: [php]
comments: true
---

## 前言

用php基础排序算法

<p id = "build"></p>

1、冒泡排序

    $arr = [5,8,2,6,15,9,7,16,10,21,13,17,4];
    $lengs = count($arr);
    for($i = 0 ; $i<$lengs ;$i++){
        for($j = 0 ;$j < $lengs -1 - $i ; $j++){
            if($arr[$j] > $arr[$j+1]){
                $news = $arr[$j];
                $arr[$j] = $arr[$j+1];
                $arr[$j+1] = $news;
            }
        }
    }
    
 输出 [2,4,5,6,7,8,9,10,13,15,16,17,21] ;
 
 
    


 

—— L 后记于 2019.04.03


