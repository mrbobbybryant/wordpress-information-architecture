##  Creating Custom Meta Fields

```php
/**
 * Registers the metabox for your Custom Post Type.
 */
function register_my_cool_metabox() {
	add_meta_box(
		'my-cool-meta-box',
		esc_html__( 'Metabox Title', 'textdomain' ),
		'my_cool_metabox_display',
		'custom-posttype-slug'
	);
}
```
