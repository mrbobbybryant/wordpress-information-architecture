##  Term Query Cont.

```php
'tax_query' => array(
	'relation' => 'AND',
	array(
		'taxonomy' => 'movie_genre',
		'field'    => 'slug',
		'terms'    => array( 'action', 'comedy' ),
	),
	array(
		'taxonomy' => 'actor',
		'field'    => 'term_id',
		'terms'    => array( 103, 115, 206 ),
		'operator' => 'NOT IN',
	),
)
```
