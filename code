<?php

function wikiplus_block_http_request_domains($preempt, $r, $url)
{
    $blocked_domains = array(
        'wordpress.com',
        'gravatar.com',
        'version.xcart.ir',
        'learndash.com',
        'gravityapi.com',
        'remote.learndash.com',
        'yoast.com',
        'bridge.unitedover.com',
        'woocommerce.ir',
        'zemez.io',
        'account.jetformbuilder.com',
        'github.com',
        'yoa.st',
        'w.org',
        'unyson.io',
        'siteorigin.com',
        'woocommerce.com',
        'cdn.jsdelivr.net',
        'cdn.themesinfo.com',
        'themesinfo.com',
        'my.yoast.com',
        'currencies.yithemes.com',
        'yithemes.com',
        'jsdelivr.net',
        'unpkg.com',
        'cdnjs.cloudflare.com',
        'ajax.googleapis.com',
        'dl3.wpnovin.com',
        'secure.gravatar.com',
        'api.crocoblock.com',
        'relevanssi.com',
        'plugins.morningtrain.dk',
        'connect.advancedcustomfields.com',
        'xcart.ir',
        'translate.wordpress.com',
        'joomunited.com',
        'wp-rocket.me',
        'wpmelon-updates.com',
        'nikanadv.ir',
        'themeisle.com',
        'www.arformsplugin.com',
        'wpshout.com',
        'www.codeinwp.com',
        'ipecho.net',
        'ident.me'
    );

    foreach ($blocked_domains as $blocked_domain) {
        if (strpos($url, $blocked_domain) !== false) {
            return new WP_Error('http_request_blocked', 'Requests to this domain are blocked.');
        }
    }

    return $preempt;
}
add_filter('pre_http_request', 'wikiplus_block_http_request_domains', 10, 3);
