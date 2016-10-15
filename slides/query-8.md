##  Query by Metadata

```php
$args = array(
	'meta_value' => 'blue',
	'post_type'  => 'page'
);
$query = new WP_Query( $args );
```
```php
$args = array(
	'meta_key'     => 'color',
	'meta_value'   => 'blue',
	'meta_compare' => '!='
);
$query = new WP_Query( $args );
```
