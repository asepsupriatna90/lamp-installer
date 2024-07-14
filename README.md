#!/bin/bash

# Function to install LAMP on Ubuntu/Debian
install_ubuntu() {
    echo "Updating package list..."
    sudo apt update -y

    echo "Installing Apache..."
    sudo apt install apache2 -y

    echo "Installing MySQL..."
    sudo apt install mysql-server -y

    echo "Installing PHP..."
    sudo apt install php libapache2-mod-php php-mysql -y

    echo "Restarting Apache to apply changes..."
    sudo systemctl restart apache2

    echo "LAMP stack installed successfully on Ubuntu/Debian!"
}

# Function to install LAMP on CentOS/RHEL
install_centos() {
    echo "Updating package list..."
    sudo yum update -y

    echo "Installing Apache..."
    sudo yum install httpd -y

    echo "Installing MySQL (MariaDB)..."
    sudo yum install mariadb-server mariadb -y

    echo "Installing PHP..."
    sudo yum install php php-mysql -y

    echo "Starting Apache and MariaDB services..."
    sudo systemctl start httpd
    sudo systemctl start mariadb

    echo "Enabling Apache and MariaDB to start on boot..."
    sudo systemctl enable httpd
    sudo systemctl enable mariadb

    echo "LAMP stack installed successfully on CentOS/RHEL!"
}

# Function to install LAMP on Fedora
install_fedora() {
    echo "Updating package list..."
    sudo dnf update -y

    echo "Installing Apache..."
    sudo dnf install httpd -y

    echo "Installing MySQL (MariaDB)..."
    sudo dnf install mariadb-server mariadb -y

    echo "Installing PHP..."
    sudo dnf install php php-mysqlnd -y

    echo "Starting Apache and MariaDB services..."
    sudo systemctl start httpd
    sudo systemctl start mariadb

    echo "Enabling Apache and MariaDB to start on boot..."
    sudo systemctl enable httpd
    sudo systemctl enable mariadb

    echo "LAMP stack installed successfully on Fedora!"
}

# Detect the OS and call the respective function
if [ -f /etc/os-release ]; then
    . /etc/os-release
    case "$ID" in
        ubuntu|debian)
            install_ubuntu
            ;;
        centos|rhel)
            install_centos
            ;;
        fedora)
            install_fedora
            ;;
        *)
            echo "Unsupported Linux distribution."
            exit 1
            ;;
    esac
else
    echo "Cannot detect the OS."
    exit 1
fi
