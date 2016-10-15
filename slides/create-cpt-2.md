##  Create CPT Cont.

```php
$args = array(
	'labels' => $labels,
	'public' => true,
	'description' => esc_html__( 'Offices', 'textdomain' ),
	'hierarchical' => true,
	'has_archive'  => false,
	'menu_position' => 10,
	'menu_icon'     => 'dashicons-building',
	'rewrite'       => array(
		'slug'       => 'location'
	),
	'supports' => array(
		'title',
		'thumbnail',
		'editor'
	)
);
```
