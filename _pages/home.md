---
layout: home
permalink: /
author:
  name             : "乐翁"
  avatar           : "/assets/images/Phuket Beach.jpg" # /assets/images/普吉岛海滩.jpg" # path of avatar image, e.g. "/assets/assets/images/bio-photo.jpg"
  bio              : "Don't stop"
author_profile: true
hidden: true
# sidebar:
#   nav: "docs"
header:
  # overlay_color: "#5e616c"
  overlay_image: /assets/images/road.jpg
  # image: /assets/images/road.jpg
  # og_image: /assets/images/cat.png
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



# feature_row:
#   - image_path: /assets/images/road.jpg
#     alt: "customizable"
#     title: "Super customizable"
#     excerpt: "Everything from the menus, sidebars, comments, and more can be configured or set with YAML Front Matter."
#     url: "/docs/configuration/"
#     btn_class: "btn--primary"
#     btn_label: "Learn more"
#   - image_path: /assets/images/road.jpg
#     alt: "fully responsive"
#     title: "Responsive layouts"
#     excerpt: "Built with HTML5 + CSS3. All layouts are fully responsive with helpers to augment your content."
#     url: "/docs/layouts/"
#     btn_class: "btn--primary"
#     btn_label: "Learn more"
#   - image_path: /assets/images/road.jpg
#     alt: "100% free"
#     title: "100% free"
#     excerpt: "Free to use however you want under the MIT License. Clone it, fork it, customize it... whatever!"
#     url: "/docs/license/"
#     btn_class: "btn--primary"
#     btn_label: "Learn more"      

---

{% include feature_row %}

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
