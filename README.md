<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <title>Geodesu</title>
  <script src="./mermaid.js"></script>
</head>
<body>
  <a href="#">Основное окно управоленя</a> | <a href="#">Состояния нефтебаз</a> | <a href="#">Список движа на складе</a>
  <div class="mermaid">
	gantt
	dateFormat  YYYY-MM-DD
	title Доставка топлива на нефтебазу Хандыга

	section Головной офис
	Оплатить счет  НПЗ        :done,    des1, 2019-01-01,2019-01-08
	Взять в аренду цистерны   :active,  des2, 2019-01-09, 14d
	Отправить топливо в НБ    :active,  des3, after des2, 14d
	Ждать разругрзки топлива  :         des4, after des3, 5d
	
	section Нижний бестях
	Получить топливо на хранение   :active,    des5, after des2, 14d
	Отгрузить топливо в НБ ХАНДЫГА :active,    des6, after des2, 14d
	Отдать цистерны         	   :active,    des7, after des5, 14d
	
	section Хандыга
	Получить топливо на хранение   :active,    des8, after des2, 14d
	
	
  
  </div>
  <script>
    mermaid.initialize({
      theme: 'forest',
      // themeCSS: '.node rect { fill: red; }',
      logLevel: 3,
      flowchart: { curve: 'linear' },
      gantt: { axisFormat: '%m/%d/%Y' },
      sequence: { actorMargin: 50 },
      // sequenceDiagram: { actorMargin: 300 } // deprecated
    });
  </script>
</body>
</html>
