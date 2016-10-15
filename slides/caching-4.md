##  Transients Cont.

```php
function get_homepage_blog_post() {

	$posts = get_transient( 'homepage-recent_posts' );

	if ( empty( $posts ) ) {
		$posts = fetch_homepage_posts();

		if ( ! $results->have_posts() ) {
			$results = set_transient( 'homepage-recent_posts', $posts->posts; );
		}

	}

	return $posts;
}
```
