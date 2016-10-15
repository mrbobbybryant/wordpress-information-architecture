##  pre_get_posts

Allows you to modify the main query.

```php
function set_posts_per_page( $query ) {

	if ( is_admin() || ! $query->is_main_query() )
		return;

	if ( is_home() || is_archive() || is_search() ) {
		$query->set( 'posts_per_page', 9 );
		return;
	}
}
```
