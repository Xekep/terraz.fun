---
layout: page
title: Администраторы
image:
  feature: abstract-5.jpg
  #credit: dargadgetz
  #creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: false
---

<script>
window.onload =  function() {
  $.ajax({
      type: "GET",
      cache: false,
      async: false,
      url: "http://sc.terraz.ru/admins.php",
      success: function(data){
          if(data != ""){
              $('#adm_table').append(data);
           }
       }
   });
}
</script>

<center>**Супер администратор:** Ketrin :smile_cat:</center>

<div id="adm_table" align="center"></div>
