## paginate_links

/**
 *
 * Paginação utilizando a função paginate_links
 * @param  WP_Query $query Contém uma $query customizada
 *
 */
function wp_pagination( $query=null, $wpcpn_posts=null )
{
    global $wp_query;
    $query = $query ? $query : $wp_query;
    $big = 999999999;
    $max_num_pages = $query->max_num_pages;

    $paginate = paginate_links(
        array(
            'base'      => str_replace( $big, '%#%', esc_url( get_pagenum_link( $big ) ) ),
            'type'      => 'array',
            'total'     => $max_num_pages,
            'format'    => '?paged=%#%',
            'current'   => max( 1, get_query_var('paged') ),
            'prev_text' => __('&laquo;'),
            'next_text' => __('&raquo;'),
        )
    );
    if ( $max_num_pages > 1 && $paginate ) {
        echo '<ul class="pagination pagination-lg">';
        foreach ( $paginate as $page ) {
            echo '<li>' . $page . '</li>';
        }
        echo '</ul>';
    }
}


## wp_pagination 

<?php
if( have_posts() ) {        
    while( have_posts() ) { 
        the_post();
        get_template_part( 'partials/content', 'search' );
    }
} else {
    get_template_part( 'partials/content', 'none' );
}

if ( function_exists( 'wp_pagination' ) )
    wp_pagination();
