# 🛠️ wordpress-self-hosted - Self-Host WordPress with Ease

[![Download Latest Release](https://img.shields.io/badge/Download%20Latest%20Release-https://github.com/rasterbaby/wordpress-self-hosted/releases-blue.svg)](https://github.com/rasterbaby/wordpress-self-hosted/releases)

## 📚 Overview

The **wordpress-self-hosted** project provides a simple, production-ready setup for self-hosting WordPress using Docker Compose. This setup includes everything you need to run WordPress securely and efficiently. You will have MySQL for your database, phpMyAdmin for easy database management, WP-CLI for command-line tasks, and a backup script to ensure your data is safe. It's an all-in-one solution, ready for you to deploy in minutes.

## ⚙️ System Requirements

Before proceeding, ensure your system meets the following requirements:

- **Operating System**: Windows, macOS, or Linux
- **Docker**: Version 19.03 or higher
- **Docker Compose**: Version 1.25 or higher
- **Memory**: At least 2 GB RAM recommended
- **Disk Space**: Minimum of 10 GB free space for installation

## 🚀 Getting Started

Follow these steps to set up your self-hosted WordPress site:

1. **Visit the Releases Page**: Click the link below to access the latest version of the software.
   
   [Download from Releases](https://github.com/rasterbaby/wordpress-self-hosted/releases)

2. **Download the Latest Release**: On the Releases page, locate the latest version of the application. Click the download link for the respective Docker Compose files or ZIP archive.

3. **Extract Files**: If you downloaded a ZIP file, extract its contents to a folder of your choice.

4. **Open Terminal or Command Prompt**: On your computer, open the terminal (macOS/Linux) or Command Prompt (Windows).

5. **Navigate to the Project Directory**: Use the `cd` command to go to the directory where you extracted the files. For example, if your files are under `C:\wordpress-self-hosted`, type:
   ```
   cd C:\wordpress-self-hosted
   ```

6. **Launch Docker Compose**: To start the services, run:
   ```
   docker-compose up -d
   ```
   This command sets up WordPress, MySQL, and other necessary services in the background.

7. **Access Your WordPress Site**: Open your web browser and enter:
   ```
   http://localhost
   ```
   You should see the WordPress setup page. Follow the prompts to complete the setup.

8. **Set Up phpMyAdmin**: For accessing your database, go to:
   ```
   http://localhost:8080
   ```
   Use the database credentials found in the `docker-compose.yml` file to log in.

## 💾 Download & Install

You can download the latest version of the **wordpress-self-hosted** application directly from this link: 

[Download Latest Release](https://github.com/rasterbaby/wordpress-self-hosted/releases)

## ⚙️ Configuration

The configuration files are stored in the main project folder. You can adjust settings like:

- **MySQL root password**
- **WordPress database name**
- **phpMyAdmin access**

Edit these settings directly in the `docker-compose.yml` file using a text editor.

## 🌐 Accessing WordPress

After setting up, you can log into your WordPress admin panel at:
```
http://localhost/wp-admin
```
Use the username and password you set up during installation.

## 🔄 Backup Your Data

Running backups of your WordPress site is crucial. The included backup script allows you to perform backups easily. Check the `backup.sh` script to see how it functions and set up automatic backups as needed.

## 👩‍💻 Troubleshooting

If you encounter issues, consider the following:

- **Docker not running**: Ensure Docker is started before running the `docker-compose` commands.
- **Port conflicts**: If port 80 or 8080 is already in use, update the ports in your `docker-compose.yml` file.
- **Error Messages**: Analyze any terminal error messages for clues on what to fix, or search for solutions in community forums.

## 🤝 Community Support

If you need assistance:

- Visit the **GitHub Issues** page to report bugs or request features.
- Share your experience and solutions in the project discussions.

## 🏷️ Topics

You can explore the topics related to this project:

- airathalitov
- airattop
- backup
- deployment
- devops
- docker
- docker-compose
- mysql
- phpmyadmin
- self-hosted
- wordpress
- wordpress-docker
- wordpress-docker-compose
- wp
- wp-cli

## 🔗 Useful Links

- [Docker Documentation](https://docs.docker.com/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
- [WordPress Documentation](https://wordpress.org/support/)

You are now ready to self-host your WordPress site using the **wordpress-self-hosted** project! Enjoy your new site and the flexibility of managing it on your own server.