## the_excerpt()

<?php 
function wpdev_custom_excerpt_length( $length ) {
 return 20;
}
add_filter( 'excerpt_length', 'wpdev_custom_excerpt_length');

?>
