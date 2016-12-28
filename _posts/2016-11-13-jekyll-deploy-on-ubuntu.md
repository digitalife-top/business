---
title:      "Jekyll deployment on VPS server big title"
description:   "Quảng cáo truyền thống có còn lợi thế so với marketing online?"
date:       2016-11-17
author:     "Vu, Nguyen"
header-img: "https://assets.entrepreneur.com/content/3x2/274/20161108193331-GettyImages-594918166.jpeg"    
keyword :   "tiêu đề bài viết seo"                 
long-keyword: "marketing online bằng tiêu đề bài viết seo"        
target-site: "http://digitalife.top"    
category: advertising
tags: ["Tiêu đề bài viết seo"]
---

<!-- BEGIN POST_EXCERPT: mo ta ngan ve noi dung bai viet -->
We have to plaug We have to plaug We have to plaug We have to plaug We have to 
plaug We have to plaug We have to plaug We have to plaug We have to plaug 
<!--more-->
<!-- END  POST_EXCERPT -->


## Deploy Jekyll site on VPS

## Create folder      

    /opt/www/domain.top/www
    /opt/www/domain.top/sub

## Copy source to that folder 

    cp -r /path-to/src /opt/www/domain.top/des 

### Edit config._yml 
    -- Edit as following: 
    url: domain.top
    baseurl: "" # empty

## Add nginx server_name on based that domain

    -- Edit /etc/nginx/sites-enabled/jekyll 
    bypass proxy to: 127.0.0.1:port
    with port from: 4001 to 4999 (999 web socketservers)

**Nginx restart**

    service nginx restart

## Re-run bash to load websocket server on ports

    -- Edit bash /opt/jekyll.sh (point right port), then run: 
    /opt/jekyll.sh

### Tips
    -- To fix LF, run: 
    dos2unix /opt/jekyll.sh 

### Test by netstat
    netstat -peanut

Thanks 


  
