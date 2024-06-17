---
layout: splash
title: 关于
permalink: /about/
header:
  overlay_image: /assets/images/road.jpg
  actions:
    - label: "<i class='fas fa-fw fa-envelope-square'></i> 32588@88.com"
      url: "mailto:32588@88.com"
    - label: "<i class='fab fa-fw fa-github'></i> GitHub"
      url: "https://github.com/Yalongduan"
    - div: 
          <div class='wechat-icon-container btn btn--light-outline btn--large'>
            <i class='fab fa-brands fa-weixin'></i> WeChat
            <div class='qr-code'>
              <img src='/assets/images/WeChat.jpg' alt='WeChat QR Code'>
            </div>
          </div>
excerpt: 
      <div class="overlay">
          <div class="current-time" id="current-time"></div>
      </div>
---

<script>
  document.addEventListener("DOMContentLoaded", function() {
      function updateTime() {
          var now = new Date();
          var days = ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'];
          var formattedTime = now.getFullYear() + '-' +
                              ('0' + (now.getMonth() + 1)).slice(-2) + '-' +
                              ('0' + now.getDate()).slice(-2) + ' ' +
                              ('0' + now.getHours()).slice(-2) + ':' +
                              ('0' + now.getMinutes()).slice(-2) + ':' +
                              ('0' + now.getSeconds()).slice(-2) + ' ' +
                              days[now.getDay()] ;
          document.getElementById('current-time').textContent = formattedTime;
      }
      updateTime();
      setInterval(updateTime, 1000); // 每秒更新一次时间
  });
</script>

## <center>忆往昔</center>
