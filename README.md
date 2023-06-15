# Ubuntu Linux Installation Guide

This guide will walk you through the step-by-step process of installing Apache2, PHP, MySQL, phpMyAdmin, fixing permission issues, fixing ownership, installing WP-CLI, and installing WordPress on an Ubuntu Linux system.

## 1. Install Apache2

To install Apache2, run the following commands:

```
sudo apt update
sudo apt install apache2
```

After installation, you can verify the Apache2 service status:

```
sudo systemctl status apache2
```

## 2. Install PHP

To install PHP and necessary modules, run the following commands:

```
sudo apt install php libapache2-mod-php php-mysql
```

Verify the PHP installation:

```
php -v
```

## 3. Install MySQL

To install MySQL, run the following command:

```
sudo apt install mysql-server
```

Follow the prompts to set up the MySQL root password.

## 4. Install phpMyAdmin

To install phpMyAdmin, run the following commands:

```
sudo apt install phpmyadmin
sudo ln -s /usr/share/phpmyadmin /var/www/html/phpmyadmin
```

Access phpMyAdmin by visiting `http://localhost/phpmyadmin` in your web browser.

## 5. Fix Permission Issues

To fix permission issues, run the following commands:

```
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
```

## 6. Fix Ownership

To fix ownership issues, run the following command:

```
sudo chown -R your_username:your_username /var/www/html
```

Replace `your_username` with your actual username.

## 7. Install WP-CLI

To install WP-CLI, run the following commands:

```
sudo apt install curl
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
chmod +x wp-cli.phar
sudo mv wp-cli.phar /usr/local/bin/wp
```

Verify the WP-CLI installation:

```
wp --info
```

## 8. Install WordPress using WP-CLI

To install WordPress using WP-CLI, navigate to the document root and run the following command:

```
wp core download --path=/var/www/html
wp core config --path=/var/www/html --dbname=your_database_name --dbuser=your_username --dbpass=your_password --dbhost=localhost --dbprefix=wp_
wp core install --path=/var/www/html --url=http://localhost --title="Your Site Title" --admin_user=admin --admin_password=admin --admin_email=admin@example.com
```

Replace `your_database_name`, `your_username`, `your_password`, and other parameters with your actual values.

Access your WordPress site by visiting `http://localhost` in your web browser.

---

Feel free to customize and expand this guide further based on your specific requirements and preferences.
