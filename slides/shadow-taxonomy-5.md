##  Shadow Taxonomy Cont.

```php
add_action( 'init', function() {
    register_taxonomy(
        'services-tax',
        'staff-cpt',
        array(
            'label'         => __( 'Services', 'text-domain' ),
            'rewrite'       => false,
            'show_tagcloud' => false,
            'hierarchical'  => true,
        )
    );
    \Shadow_Taxonomy\Core\create_relationship( 'service-cpt', 'service-tax' );
});
```
