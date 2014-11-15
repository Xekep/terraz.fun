---
layout: page
title: Диаграмма протектов
image:
  feature: abstract-5.jpg
  #credit: dargadgetz
  #creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
comments: false
---

Одним из критериев по которым мы оцениваем активность привилегированных игроков является количество установленных протектов.

<script type="text/javascript" src="http://www.google.com/jsapi"></script>
<script type="text/javascript">
      // Load the Visualization API and the piechart package.
      google.load('visualization', '1.0', {'packages':['corechart']});

      // Set a callback to run when the Google Visualization API is loaded.
      google.setOnLoadCallback(drawChart);
      // Callback that creates and populates a data table,
      // instantiates the pie chart, passes in the data and
      // draws it.
      function drawChart() {

        $.ajax({
                type : "GET",
                url : "http://sc.terraz.ru/regions.php?callback=?",
                dataType: "jsonp",
                success: function(res) {
                        if (res.offline != 1)
                        {
                                // Create the data table.
                                var data = new google.visualization.DataTable();
                                data.addColumn('string', 'Topping');
                                data.addColumn('number', 'Slices');

                        	for (var i = 0; i < res.Users.length; i++) {
                        		data.addRows([[decodeURIComponent(res.Users[i].Name), res.Users[i].Count]]);
                        	}

                                if (res.Users.length<res.Count)
                                {
                                       data.addRows([['Суперадминистраторы', res.Count - res.Users.length]]); 
                                }

                                // Set chart options
                                var options = {is3D: true,
                                        backgroundColor: 'transparent',
                                        'title':'Диаграмма протектов',
                                        'width':700,
                                        'height':600};

                                // Instantiate and draw our chart, passing in some options.
                                var chart = new google.visualization.PieChart(document.getElementById('chart_div'));
                                chart.draw(data, options);
                        }
                },
        });


      }
</script>
<center><div id="chart_div" style="background-color: transparent;"></div></center>
