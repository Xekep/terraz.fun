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
              //$jQuery("body").html(data);
              var content = "<center>";
              content += data;
              content += "</center>";
              $('#adm_table').append(content);
           }
       }
   });
}
</script>
<div id="adm_table">
<!--<iframe id="iframe1" src="http://sc.terraz.ru/admins.php" frameborder="0" marginwidth="0" marginheight="0" scrolling="no"></iframe>-->
</div>
