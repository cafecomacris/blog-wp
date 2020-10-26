## Desativando a Admin Bar no Front End

# Modo antigo
<?php 
add_filter( 'show_admin_bar', '__return_false' );
?>


# OBS:: Em versões mais recentes do WordPress (de acordo com reports dos utilizadores, 3.3 e superiores),
o filtro que remove a admin bar não funciona como deveria; portanto ao invés de usarmos:

// a solução acima ou então
show_admin_bar( false );

 # Dentro da função de setup do tema:

if ( !is_admin() )
    add_filter( 'wp_admin_bar_class', '__return_false' );
