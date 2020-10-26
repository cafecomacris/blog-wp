## Trocar o login do WordPress

add_action( 'login_enqueue_scripts', 'login_logo' );
function login_logo() {
    ?>

    <style type="text/css">
        body.login div#login h1 a {
            background-image: url("<?php echo get_template_directory_uri(); ?>/PATH_PARA_SUA_LOGO");
            padding-bottom: 0px;
            background-size: {LARGURA_DA_LOGO}px {ALTURA_LOGO}px;
            -webkit-background-size:{LARGURA_DA_LOGO}px {ALTURA_LOGO}px;
            width: {LARGURA_DA_LOGO}px;
        }
    </style>

    <?php
}
