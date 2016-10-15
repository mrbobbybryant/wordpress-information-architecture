##  Custom Meta Fields Cont.

```php
function save_my_cool_meta_box( $post_id ) {

	$is_autosave = wp_is_post_autosave( $post_id );
	$is_revision = wp_is_post_revision( $post_id );
	$is_valid_nonce = ( isset( $_POST['my_meta_box_nonce'] ) && wp_verify_nonce( $_POST[ 'my_meta_box_nonce' ], 'my_meta_box' ) );
	// Exits script depending on save status
	if ( $is_autosave || $is_revision || !$is_valid_nonce ) {
		return;
	}

	update_post_meta(
		$post_id,
		'meta-name-key',
		sanitize_text_field( $_POST[ 'meta-name-key' ] )
	);
}
add_action( 'save_post', 'save_my_cool_meta_box' );
```
