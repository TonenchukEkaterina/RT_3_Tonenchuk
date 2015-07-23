# RT_3_Tonenchuk
<html xmlns="http://www.w3.org/1999/xhtml">
 <head>    
 <title>Примеры. Добавление прямоугольника на карту.</title>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>  
    <!--         Подключаем API карт 2.x
         Параметры:
           - load=package.full - полная сборка;
        - lang=ru-RU - язык русский.     -->
      <script src="http://api-maps.yandex.ru/2.0/?load=package.full&lang=ru-RU"
             type="text/javascript"></script>
     <script type="text/javascript"> 
        ymaps.ready(init);  
        function init() { 
            var myMap = new ymaps.Map('map', { 
                center: [-25.30, -57.63], 
                zoom: 10           
 }),            
                 
 myPolygon = new ymaps.Polygon([[
                    // Координаты вершин внешней границы многоугольника.
			[-25.223217,-57.633465],
			[-25.218845,-57.531839],
			[-25.284095,-57.483000],
			[-25.357432,-57.531497],
			[-25.36055,-57.633465],
			[-25.290025,-57.680842]
                ]]);
  
            myMap.geoObjects.add(myPolygon)
                 .add(myPolygon); 
        }     </script> 
</head>  
<body> 
<h2>Добавление прямоугольника на карту</h2>  
<div id="map" style="width:600px;height:400px"></div> </body>  
</html>  
 
