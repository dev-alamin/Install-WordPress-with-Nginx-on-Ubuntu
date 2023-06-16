# Ubuntu Linux Web Development Setup Guide

This guide will walk you through the step-by-step process of setting up a web development environment on Ubuntu Linux. It includes the installation of Apache2, PHP, MySQL, phpMyAdmin, the configuration of virtual hosts for different websites, fixing permission issues, and installing WP-CLI for WordPress management.

## 1. Install Apache2

To install Apache2, run the following commands:

```bash
sudo apt update
sudo apt install apache2
```

Verify the Apache2 installation:

```bash
sudo systemctl status apache2
```

## 2. Install PHP

To install PHP and necessary modules, run the following commands:

```bash
sudo apt install php libapache2-mod-php php-mysql
```

Verify the PHP installation:

```bash
php -v
```

## 3. Install MySQL

To install MySQL, run the following command:

```bash
sudo apt install mysql-server
```

Follow the prompts to set up the MySQL root password.

## 4. Install phpMyAdmin

To install phpMyAdmin, run the following commands:

```bash
sudo apt install phpmyadmin
sudo ln -s /usr/share/phpmyadmin /var/www/html/phpmyadmin
```

Access phpMyAdmin by visiting `http://localhost/phpmyadmin` in your web browser.

### Grant Privileges to phpMyAdmin User

If you encounter any permission issues while creating a new database using phpMyAdmin, execute the following SQL commands:

```sql
GRANT ALL PRIVILEGES ON hc.* TO 'phpmyadmin'@'localhost';
FLUSH PRIVILEGES;
```

## 5. Configure Virtual Hosts

To create different domains for different sites, you can use virtual hosts in Apache. Follow these steps:

1. Create a new virtual host configuration file:

   ```bash
   sudo nano /etc/apache2/sites-available/example.com.conf
   ```

2. Add the following content to the file, replacing `example.com` with your desired domain name:

   ```apacheconf
   <VirtualHost *:80>
       ServerAdmin webmaster@example.com
       ServerName example.com
       ServerAlias www.example.com
       DocumentRoot /var/www/html/example.com
       ErrorLog ${APACHE_LOG_DIR}/error.log
       CustomLog ${APACHE_LOG_DIR}/access.log combined
   </VirtualHost>
   ```

3. Save and close the file.

4. Enable the virtual host configuration:

   ```bash
   sudo a2ensite example.com.conf
   ```

5. Restart Apache to apply the changes:

   ```bash
   sudo systemctl restart apache2
   ```

6. Create the directory for your new site:

   ```bash
   sudo mkdir /var/www/html/example.com
   ```

7. Set the necessary permissions for the directory:

   ```bash
   sudo chown -R www-data:www-data /var/www/html/example.com
   sudo chmod -R 755 /var/www/html/example.com
   ```

8. Add an entry in your `/etc/hosts` file to map the domain to your localhost:

   ```bash
   sudo nano /etc/hosts
   ```

   Add the following line:

   ```
   127.0.0.1 example.com www.example.com
   ```

   Save and close the file.

9. Now you can access your site by visiting `http://example.com` or `http://www.example.com` in your web browser.

Repeat steps 1 to 9 for each new site you want to create with a different domain name. Each virtual host configuration file should have a unique name and corresponding directory.

## 6. Fix Permission Issues



To fix permission issues, run the following commands:

```bash
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
```

## 7. Install WP-CLI

To install WP-CLI, run the following commands:

```bash
sudo apt install curl
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
chmod +x wp-cli.phar
sudo mv wp-cli.phar /usr/local/bin/wp
```

Verify the WP-CLI installation:

```bash
wp --info
```

## 8. Install WordPress using WP-CLI

To install WordPress using WP-CLI, navigate to the document root and run the following command:

```bash
wp core download --path=/var/www/html
wp core config --path=/var/www/html --dbname=your_database_name --dbuser=your_username --dbpass=your_password --dbhost=localhost --dbprefix=wp_
wp core install --path=/var/www/html --url=http://localhost --title="Your Site Title" --admin_user=admin --admin_password=admin --admin_email=admin@example.com
```

Replace `your_database_name`, `your_username`, `your_password`, and other parameters with your actual values.

Access your WordPress site by visiting `http://localhost` in your web browser.

---

Feel free to customize and expand this guide further based on your specific requirements and preferences.
