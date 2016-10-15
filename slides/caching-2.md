##  Transients

```php
$posts = get_transient( 'my-key-name' );
```

```php
$results = new WP_Query( $args );
set_transient( 'key-name', $results, 12 * HOUR_IN_SECONDS );
```

Note:
Transients are saved in the options table.
Can still be more performant on complex or poor performing queries.
Will Be stored in object cache automatically if an in memory datastore is present.
