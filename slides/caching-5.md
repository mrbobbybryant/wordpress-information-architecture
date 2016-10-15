##  Transients Cont.

```php
add_action( 'save_post_' . 'cpt-slug', function() {
	$blogs = fetch_homepage_blogs();
	set_transient( 'homepage-recent_posts', $blogs );
} );
```
