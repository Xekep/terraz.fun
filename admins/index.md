---
layout: page
title: Администраторы
comments: false
---

<script>
window.onload =  function() {
  $.ajax({
      type: "GET",
      url: "https://service.terraria-z.ru/admins.php",
	  dataType: "jsonp",
      success: function(data){
          if(data != ""){
              renderTable(data);
           }
       }
   });
}
function renderTable(data)
{
	$("#vip").append(array2table(data.vip));
	$("#help").append(array2table(data.help));
	$("#newadmin").append(array2table(data.newadmin));
	$("#admin").append(array2table(data.admin));
	$("#trustedadmin").append(array2table(data.trustedadmin));
	$("#vipadmin").append(array2table(data.vipadmin));
	$("#vipstadmin").append(array2table(data.vipstadmin));
	$("#vipgladmin").append(array2table(data.vipgladmin));
}

function array2table(data)
{
   var tbl_body = "";
    $.each(data, function() {
        var tbl_row = "";
        $.each(this, function(k , v) {
            tbl_row += "<td>"+v+"</td>";
        })
        tbl_body += "<tr>"+tbl_row+"</tr>";                 
    });
    return tbl_body;
}
</script>
<div align="center" markdown="1">
**Супер администратор:** Ketrin
</div>
<div align="center">
<table id="vip"><caption>VIP</caption></table>
<table id="help"><caption>Helper</caption></table>
<table id="newadmin"><caption>Admin</caption></table>
<table id="admin"><caption>St.Admin</caption></table>
<table id="trustedadmin"><caption>Gl.Admin</caption></table>
<table id="vipadmin"><caption>Vip-Admin</caption></table>
<table id="vipstadmin"><caption>Vip-St.Admin</caption></table>
<table id="vipgladmin"><caption>Vip-Gl.Admin</caption></table>
</div>
