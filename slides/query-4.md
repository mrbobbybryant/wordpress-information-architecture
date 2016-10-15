##  get_posts cont.

```php
function get_posts( $args = null ) {
	...
	$get_posts = new WP_Query;
	return $get_posts->query($r);
}
```
