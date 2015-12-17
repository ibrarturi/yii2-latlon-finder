LatLngFinder
============
Find Latitude and Longitude using Google Maps

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist ibrarturi/yii2-latlng-finder "dev-master"
```

or add

```
"ibrarturi/yii2-latlng-finder": "dev-master"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code mentioned below. 
Click once on the map to the get the marker and coordinates then you can drag the marker around to the desired place on the map.

 * Default usage

```php
<div class="form-group">
    <label class="control-label" for="lat">Latitude</label>
    <input class="form-control" type="text" name="lat" id="lat">
</div>
<div class="form-group">
    <label class="control-label" for="lng">Longitude</label>
    <input class="form-control" type="text" name="lng" id="lng">
</div>
<div class="form-group">
    <label class="control-label" for="zoom">Zoom</label>
    <input class="form-control" type="text" name="zoom" id="zoom">
</div>

<?= \ibrarturi\latlngfinder\LatLngFinder::widget(); ?>
```

 * Default usage without Zoom Field

```php
<div class="form-group">
    <label class="control-label" for="lat">Latitude</label>
    <input class="form-control" type="text" name="lat" id="lat">
</div>
<div class="form-group">
    <label class="control-label" for="lng">Longitude</label>
    <input class="form-control" type="text" name="lng" id="lng">
</div>

<?= \ibrarturi\latlngfinder\LatLngFinder::widget([
	'enableZoom' => false 			// true, false
]); ?>
```
 
 * Default usage with optional parameters

```php
<div class="form-group">
    <label class="control-label" for="lat">Latitude</label>
    <input class="form-control" type="text" name="lat" id="lat">
</div>
<div class="form-group">
    <label class="control-label" for="lng">Longitude</label>
    <input class="form-control" type="text" name="lng" id="lng">
</div>
<div class="form-group">
    <label class="control-label" for="zoom">Zoom</label>
    <input class="form-control" type="text" name="zoom" id="zoom">
</div>

<?= \ibrarturi\latlngfinder\LatLngFinder::widget([
	'latAttribute' => 'lat',		// Latitude text field id
	'lngAttribute' => 'lng',		// Longitude text field id
	'zoomAttribute' => 'zoom',		// Zoom text field id
	'mapCanvasId' => 'map',			// Map Canvas id
	'mapWidth' => 450,				// Map Canvas width
	'mapHeight' => 300,				// Map Canvas mapHeight
	'defaultLat' => -34.397,		// Default latitude for the map
	'defaultLng' =>150.644,			// Default Longitude for the map
	'defaultZoom' => 8, 			// Default zoom for the map
	'enableZoomField' => true,		// True: for assigning zoom values to the zoom field, False: Do not assign zoom value to the zoom field
]); ?>
```

 * Default usage with model

```php
<?= $form->field($model, 'lat') ?>
<?= $form->field($model, 'lng') ?>
<?= $form->field($model, 'zoom') ?>

<?= \ibrarturi\latlngfinder\LatLngFinder::widget([
    'model' => $model,				// model object
]); ?>

 ```

  * Default usage with model without zoom field

```php
<?= $form->field($model, 'lat') ?>
<?= $form->field($model, 'lng') ?>

<?= \ibrarturi\latlngfinder\LatLngFinder::widget([
    'model' => $model,				// model object
    'enableZoom' => false 			// true, false
]); ?>

 ```

 * Default usage with model and optional parameters

```php
<?= $form->field($model, 'lat') ?>
<?= $form->field($model, 'lng') ?>
<?= $form->field($model, 'zoom') ?>

<?= \ibrarturi\latlngfinder\LatLngFinder::widget([
	'model' => $model,				// model object
	'latAttribute' => 'lat',		// Latitude attribute
	'lngAttribute' => 'lng',		// Longitude attribute
	'zoomAttribute' => 'zoom',		// Zoom text attribute
	'mapCanvasId' => 'map',			// Map Canvas id
	'mapWidth' => 450,				// Map Canvas width
	'mapHeight' => 300,				// Map Canvas mapHeight
	'defaultLat' => -34.397,		// Default latitude for the map
	'defaultLng' =>150.644,			// Default Longitude for the map
	'defaultZoom' => 8, 			// Default zoom for the map
	'enableZoomField' => true,		// True: for assigning zoom values to the zoom field, False: Do not assign zoom value to the zoom field
]); ?>
```

Resources
------

 * [Project Page](https://developers.google.com/maps/documentation/javascript/examples/)
 * [Demo](http://ituri.net/gmap/latlongfinder)
 * [Github](https://github.com/ibrarturi/yii2-latlon-finder)
