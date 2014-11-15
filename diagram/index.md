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
{% raw %}
    <script src="http://www.google.com/jsapi"></script>
    <script>
      // Load the Visualization API and the piechart package.
      google.load('visualization', '1.0', {'packages':['corechart']});

      // Set a callback to run when the Google Visualization API is loaded.
      google.setOnLoadCallback(drawChart);
      // Callback that creates and populates a data table,
      // instantiates the pie chart, passes in the data and
      // draws it.
      function drawChart() {

        // Create the data table.
        var data = new google.visualization.DataTable();
        data.addColumn('string', 'Topping');
        data.addColumn('number', 'Slices');
        data.addRows([
		['/dev/null6', 1],
		['1ta41', 15],
		['A.N.D.R.E.W', 3],
		['Deez', 27],
		['DotNas', 7],
		['Lambo', 4],
		['Leon', 4],
		['Maf', 5],
		['Midorima', 1],
		['Mira', 10],
		['Mr.Andre', 2],
		['Pokerman', 1],
		['Rico', 13],
		['Serj Tankyano', 5],
		['St.Art', 5],
		['Tuk', 3],
		['Vitya', 1],
		['_Bl@ck_fOx_', 1],
		['iks', 8],
		['jTerror', 11],
		['ЕжИК', 4],
		['Икс', 1],
		['Супер администраторы', 42]
        ]);

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
    </script>
<center><div id="chart_div" style="background-color: transparent;"></div></center>
% endraw %}
