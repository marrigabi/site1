# Configurar os Sites no Servidor
Configuração do Apache

# Configurar Host Virtual para MkDocs:

- Crie um arquivo de configuração em /etc/apache2/sites-available/site1.conf:

apache

<VirtualHost *:80>
    ServerName site1.exemplo.com
    DocumentRoot /caminho/para/site1
    <Directory /caminho/para/site1>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
Configurar Host Virtual para WordPress:
Crie um arquivo de configuração em /etc/apache2/sites-available/site2.conf:

apache

<VirtualHost *:80>
    ServerName site2.exemplo.com
    DocumentRoot /var/www/html/site2
    <Directory /var/www/html/site2>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>

Habilitar os Sites:
```sh

sudo a2ensite site1.conf
sudo a2ensite site2.conf
sudo systemctl restart apache2

# Configuração do Nginx (Opcional)
Se preferir usar Nginx, siga as instruções de configuração de blocos de servidor descritas anteriormente.

Configurar o DNS
Configure os registros DNS para que site1.exemplo.com e site2.exemplo.com apontem para o IP da VM.