##  Metadata Query Cont.

```php
$args = array(
	'post_type'  => 'product',
	'meta_query' => array(
		array(
			'key'     => 'color',
			'value'   => 'blue',
			'compare' => 'NOT LIKE',
		),
	),
);
$query = new WP_Query( $args );
```
