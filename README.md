ThaiYearFormatter
=================
Convert Year to Thai Buddhist Era 

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist dixonsatit/yii2-thai-year-formatter "*"
```

or add

```
"dixonsatit/yii2-thai-year-formatter": "*"
```

to the require section of your `composer.json` file.

Config
------

```
//'language'=>'th', //  uncomment  if you want set default language to th
'components' => [
	//...
    'formatter'=>[
        'class'=>'dixonsatit\thaiYearFormatter\ThaiYearFormatter',
    ],
]
```

Usage
-----

Once the extension is installed, simply use it in your code by  :


```php
$time = time();

Yii::$app->formatter->locale = 'en-US';
echo Yii::$app->formatter->asDate($time, 'short')."<br>";
echo Yii::$app->formatter->asDate($time, 'medium')."<br>";
echo Yii::$app->formatter->asDate($time, 'long')."<br>";
echo Yii::$app->formatter->asDate($time, 'full')."<br>";

Yii::$app->formatter->locale = 'th';
echo Yii::$app->formatter->asDate($time, 'short')."<br>";
echo Yii::$app->formatter->asDate($time, 'medium')."<br>";
echo Yii::$app->formatter->asDate($time, 'long')."<br>";
echo Yii::$app->formatter->asDate($time, 'full')."<br>";

```

preview

```
6/25/15
Jun 25, 2015
June 25, 2015
Thursday, June 25, 2015

25/6/2558
25 มิ.ย. 2558
25 มิถุนายน 2558
วันอาทิตย์ที่ 25 มิถุนายน ค.ศ. 2558
```

