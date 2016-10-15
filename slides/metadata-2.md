##  Creating Custom Meta Fields Cont.

```php
function my_cool_metabox_display( $post ) {
	wp_nonce_field( 'my_meta_box', 'my_meta_box_nonce' );
	?>

	<table class="form-table">
		<tbody>
			<tr>
				<th scope="row">
					<label for="meta-key-name">
						<?php esc_html_e( 'Education', 'graydon' ); ?>
					</label>
				</th>
				<td>
					<textarea id="meta-key-name" name="meta-name-key" class="widefat" cols="50" rows="4">
					<?php echo wp_kses_post( get_post_meta( $post->ID, 'meta-name-key', true ) ); ?>
					</textarea>
				</td>
			</tr>
		</tbody>
	</table>
	<?php
}
```
