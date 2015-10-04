PHP-Minecraft-Rcon
==================

Simple Rcon class for php.

Connection is established over TCP.

Available on https://packagist.org/packages/goldman40/php-rcon-minecraft

## Examples

For this script to work, rcon must be enabled on the server, by setting `enable-rcon=true` in the server's `server.properties` file. A password must also be set, and provided in the script.

```php
use thedudeguy\Rcon;

$host = 'some.minecraftserver.com'; // Server host name or IP
$port = 25567;                      // Port rcon is listening on
$password = 'server-rcon-password'; // rcon.password setting set in server.properties
$timeout = 3;                       // How long to timeout. Default 3

$rcon = new Rcon($host, $port, $password, $timeout);

if ($rcon->connect())
{
  $rcon->send_command("say Hello World!");
}
```
