Elasticsearch Query and ActiveRecord for Yii 2
==============================================

This extension provides the [elasticsearch](http://www.elasticsearch.org/) integration for the Yii2 framework.
It includes basic querying/search support and also implements the `ActiveRecord` pattern that allows you to store active
records in elasticsearch.

For license information check the [LICENSE](LICENSE.md)-file.

Requirements
------------

elasticsearch version 1.0 or higher is required.

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist yiisoft/yii2-elasticsearch
```

or add

```json
"yiisoft/yii2-elasticsearch": "~2.0.0"
```

to the require section of your composer.json.

Configuration
-------------

To use this extension, you have to configure the Connection class in your application configuration:

```php
return [
    //....
    'components' => [
        'elasticsearch' => [
            'class' => 'yii\elasticsearch\Connection',
            'nodes' => [
                ['http_address' => '127.0.0.1:9200'],
                // configure more hosts if you have a cluster
            ],
        ],
    ]
];
```
