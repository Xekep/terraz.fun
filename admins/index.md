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
	$("#builder").append(array2table(data.builder));
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
<table>
  <tr style="vertical-align: top;">
    <td>
        <table id="vip">
          <caption><b>VIP</b></caption>
        </table>
    </td>
    <td>
        <table id="help">
          <caption><b>Helper</b></caption>
        </table>
    </td>
    <td>
        <table id="builder">
          <caption><b>Builder</b></caption>
        </table>
    </td>
  </tr>
</table>

<table>
  <tr style="vertical-align: top;">
    <td>
        <table id="newadmin">
          <caption><b>Admin</b></caption>
        </table>
    </td>
    <td>
        <table id="admin">
          <caption><b>St.Admin</b></caption>
        </table>
    </td>
    <td>
        <table id="trustedadmin">
          <caption><b>Gl.Admin</b></caption>
        </table>
    </td>
  </tr>
</table>

<table>
  <tr style="vertical-align: top;">
    <td>
        <table id="vipadmin">
          <caption><b>VipAdmin</b></caption>
        </table>
    </td>
    <td>
        <table id="vipstadmin">
          <caption><b>VipSt.Admin</b></caption>
        </table>
    </td>
    <td>
        <table id="vipgladmin">
          <caption><b>VipGl.Admin</b></caption>
        </table>
    </td>
  </tr>
</table>
</div>
