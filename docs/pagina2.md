# Instale o MySQL e PHP (necessário para o WordPress):

````sh
Copiar código
sudo apt install mysql-server
sudo mysql_secure_installation
sudo apt install php libapache2-mod-php php-mysql

# Baixe e instale o WordPress:

```sh
cd /var/www/html
sudo wget https://wordpress.org/latest.tar.gz
sudo tar -xvzf latest.tar.gz
sudo mv wordpress site2
sudo chown -R www-data:www-data site2
sudo chmod -R 755 site2

# Configure o MySQL para o WordPress:

````sh
sudo mysql -u root -p
Dentro do prompt do MySQL:

sql
````sh
CREATE DATABASE wordpress;
CREATE USER 'wpuser'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON wordpress.* TO 'wpuser'@'localhost';
FLUSH PRIVILEGES;
EXIT;