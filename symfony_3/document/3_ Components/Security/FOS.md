```XML
/var/www/html/mccp-xchange/vendor/friendsofsymfony/oauth-server-bundle/Resources/config/routing/token.xml

<route id="fos_oauth_server_token" path="/oauth/v2/token" methods="GET POST">
    <default key="_controller">fos_oauth_server.controller.token:tokenAction</default>
</route>
```

```PHP
vendor/friendsofsymfony/oauth-server-bundle/Controller/TokenController.php

class TokenController
{
    public function tokenAction(Request $request)
    {
        ...
    }
}
```