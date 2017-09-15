# amintado-global-functions
Global Functions For Use In Yii2 Web Applications For Persian Users and amintado extensions users

##install with composer
````
$ composer requere amintado/yii2-amintado-global-functions "*"
````
OR
````
$ php composer.phar requere amintado/yii2-amintado-global-functions "*"
````
OR 


add this line to 'require' section in **composer.json** file
````
"amintado/yii2-amintado-global-functions": "*"
````
##config in Yii2
add this code under **component** in main.config file in your Yii2 application:
``````
'functions'=>[
            'class'=>'amintado\base\AmintadoFunctions',
            'telegram_bot' => '@Your_Bot_ID'
        ]
``````