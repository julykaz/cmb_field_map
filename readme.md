# CMB2 Field Type: Google Maps

## Description

Google Maps field type for [CMB2](https://github.com/WebDevStudios/CMB2).

The `pw_map` field stores the latitude/longitude values which you can then use to display a map in your theme.

## Installation

Install in a theme using composer:
```json
{
 "require": {
    "php": ">=5.3.0",
    "composer/installers": "v1.0.12",
    "webdevstudios/cmb2": "dev-master",
    "julykaz/cmb_field_map": "dev-master"
  },
  "autoload": {
    "files": [
      "vendor/cmb2/init.php",
      "vendor/cmb_field_map/cmb-field-map.php"
    ]
  },
  "extra": {
    "installer-paths": {
      "vendor/{$name}/": [
        "webdevstudios/cmb2",
        "julykaz/cmb_field_map"
      ]
    }
  } 
}
```

## Usage

### `pw_map`

Save a location on a map. Example:

```php
array(
	'name' => 'Location',
	'desc' => 'Drag the marker to set the exact location',
	'id' => $prefix . 'location',
	'type' => 'pw_map',
	// 'split_values' => true, // Save latitude and longitude as two separate fields
),
```

#### Extra Parameters:

* `split_values` Save the latitude/longitude values into two custom fields, they will be stored as `$id . '_latitude'` and `$id . '_longitude'`.

## Screenshot

![Image](screenshot-1.png?raw=true)