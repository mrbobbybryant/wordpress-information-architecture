##  Query by Term

```php
$args = [
	'post_type'         => custom-post-type-slug,
	'post_status'       => 'publish',
	'posts_per_page'    => 25,
	'order'             => 'ASC',
	'tax_query' => array(
		array(
				'taxonomy' => 'taxonomy-slug',
				'field'    => 'slug',
				'terms'    => 'term-slug'
		)
	)
];

$results = new \WP_Query( $args );
```
