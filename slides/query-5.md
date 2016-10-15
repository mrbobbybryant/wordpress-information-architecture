##  WP_Query

```php
$args = [
	'post_type'         	 => 'post-type-slug',
	'post_status'       	 => 'publish',
	'posts_per_page'    	 => 25,
	'order'             	 => 'ASC',
	'no_found_rows' 		 => true,
	'update_post_meta_cache' => false,
	'update_post_term_cache' => false,
	'fields' 				=> 'ids'
];

$staff = new \WP_Query( $args );
```

Note:

Useful when pagination is not needed.
Useful when post meta will not be utilized.
Useful when taxonomy terms will not be utilized.
Useful when only the post IDs are needed (less typical).
