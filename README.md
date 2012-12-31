Yandex Maps
==========

Yii Yandex Maps addition to allowing sozlavat map with labels and lines.

Installation and Setup
---------------------

Place the extension files in a directory 'extensions' of your application. For example, in a folder yandexmap

~~~
'ext.yandexmap.YandexMap'
~~~

Use
-----

~~~
[php]
	$this->widget('ext.yandexmap.YandexMap',array(
		'id'=>'map',
		'width'=>600,
		'height'=>400,
		'center'=>array(55.76, 37.64),
		'placemark' => array(
			array(
				'lat'=>55.8,
				'lon'=>37.8,
				'options'=>array(
					'balloonContentHeader'=>'header',
					'balloonContentBody'=>'body',
					'balloonContentFooter'=>'footer',
				)
			)
		),
		'polyline' => array(
			array('lat'=>55.80,'lon'=>37.30),
			array('lat'=>55.80,'lon'=>37.40),
            array('lat'=>55.70,'lon'=>37.30),
            array('lat'=>55.70,'lon'=>37.40),
			'options'=>array(
				'strokeWidth'=> 5 // ширина линии'
			)
		),
	));

~~~

Use Placemark
---

Placemark (метки) - можно передавать как один элемент или как группу элементов.

~~~
[php]
...
		'placemark' => array(
				'lat'=>55.8,
				'lon'=>37.8,
				'options'=>array(
					'balloonContentHeader'=>'header',
					'balloonContentBody'=>'body',
					'balloonContentFooter'=>'footer',
				)
			
		),
...

~~~

группа

~~~
[php]
...
		'placemark' => array(
			array(
				'lat'=>55.8,
				'lon'=>37.8,
				'options'=>array(
					'balloonContentHeader'=>'header',
					'balloonContentBody'=>'body',
					'balloonContentFooter'=>'footer',
				)
			),
			array(
				'lat'=>55.8,
				'lon'=>37.8,
				'options'=>array(
					'balloonContentHeader'=>'header',
					'balloonContentBody'=>'body',
					'balloonContentFooter'=>'footer',
				)
			),
		),
...

~~~

Использование Polyline
---

Polyline (ломаные линии) - можно передевать как один элемент или как грумму элементов. Координаты точер задаются массивом и может быть бесконечно много.

~~~
[php]
...
	'polyline' => array(		
		array('lat'=>55.80,'lon'=>37.30),
		array('lat'=>55.80,'lon'=>37.40),
		array('lat'=>55.70,'lon'=>37.30),
		array('lat'=>55.70,'lon'=>37.40),
		'options'=>array(
			'strokeWidth'=> 5 // ширина линии
		)
	)
...

~~~

группа

~~~
[php]
...
	'polyline' => array(
		array(
			array('lat'=>55.80,'lon'=>37.30),
			array('lat'=>55.80,'lon'=>37.40),
			array('lat'=>55.70,'lon'=>37.30),
			array('lat'=>55.70,'lon'=>37.40),
			'options'=>array(
				'strokeWidth'=> 5 // ширина линии
			)
		),
		array(
			array('lat'=>55.80,'lon'=>37.30),
			array('lat'=>55.80,'lon'=>37.40),
			array('lat'=>55.70,'lon'=>37.30),
			array('lat'=>55.70,'lon'=>37.40),
			'options'=>array(
				'strokeWidth'=> 5 // ширина линии
			)
		),
	),
...

~~~