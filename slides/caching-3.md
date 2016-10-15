##  Transients Cont.

```php
function get_posts_by_category( $slug, $post_id ) {
	$key = sprintf( '%s-%d-recent_posts', $slug, absint( $post_id ) );
	$posts = get_transient( $key );

	if ( empty( $posts ) ) {
		$results = fetch_posts_by_category( $slug, $post_id );

		if ( ! $results->have_posts() ) {
			$results = fetch_recent_posts( $post_id );
		}
		$posts = $results->posts;
		set_transient( $key, $posts, 12 * HOUR_IN_SECONDS );
	}

	return $posts;
}
```
