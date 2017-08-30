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
    $.each(data, function(k, v) {
		var tbl_row = "<td>"+v+"</td>";
        tbl_body += "<tr>"+tbl_row+"</tr>";                 
    });
    return tbl_body;
}
</script>
<div align="center" markdown="1">
**Супер администратор:** Ketrin
</div>
<div align="center">
<table id="vip"><caption><b>VIP</b></caption></table>
<table id="help"><caption><b>Helper</b></caption></table>
<table id="newadmin"><caption><b>Admin</b></caption></table>
<table id="admin"><caption><b>St.Admin</b></caption></table>
<table id="trustedadmin"><caption><b>Gl.Admin</b></caption></table>
<table id="vipadmin"><caption><b>Vip-Admin</b></caption></table>
<table id="vipstadmin"><caption><b>Vip-St.Admin</b></caption></table>
<table id="vipgladmin"><caption><b>Vip-Gl.Admin</b></caption></table>
</div>
