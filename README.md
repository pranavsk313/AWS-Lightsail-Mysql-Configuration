# AWS Mini Project: Deploy and Configure an Amazon Lightsail MySQL Database

## 1. Overview

This project demonstrates the deployment and configuration of an Amazon Lightsail MySQL database. Amazon Lightsail provides a reliable and performant virtual server environment with an intuitive management console. With preconfigured Linux and Windows application stacks, Lightsail offers a simplified approach to hosting databases and applications.

In this project, we have deployed a MySQL database on Amazon Lightsail. The database instance can be utilized by any Lightsail instances or applications deployed within the same AWS Region. We have added an additional database and user, connected remotely from a Lightsail Ubuntu instance, and configured various database settings including snapshots.

![image](https://github.com/pranavsk313/AWS-Lightsail-Mysql-Configuration/assets/122976840/0a6f6c17-66c5-41a8-b78b-25596da32170)


## 2. Features

- Deployed a MySQL database on Amazon Lightsail.
- Added an additional database and user.
- Connected remotely from a Lightsail Ubuntu instance.
- Configured additional database settings and snapshots.
- Demonstrated how to view database metrics.

## 3. Prerequisites

Before starting this project, you will need:

- An active AWS account.
- Basic knowledge of Amazon Lightsail and MySQL.

## 4. Usage

1. **Deployment**: Follow the provided instructions to deploy a MySQL database on Amazon Lightsail.
2. **Configuration**: Customize database settings, add users, and create snapshots as per your requirements.
3. **Remote Connection**: Connect remotely to the Lightsail MySQL database from a Lightsail Ubuntu instance or any MySQL client.
4. **Monitoring**: Utilize Lightsail's built-in metrics to monitor the performance of your database instance.

## 5. Resources

- [Amazon Lightsail Documentation](https://lightsail.aws.amazon.com/)
- [MySQL Documentation](https://dev.mysql.com/doc/)

## 6. Steps
### ** Step 1: Create the Ubuntu instance on Amazon Lightsail**:
Click on the "Create instance" button.
    - Choose the **MySQL** blueprint for your database instance.
    - Select the instance plan based on your requirements.
    - Provide a name for your database instance and create it.

![1](https://github.com/pranavsk313/AWS-Lightsail-Mysql-Configuration/assets/122976840/c672ee50-d9b4-41b7-9358-96be1bd4811b)

![3](https://github.com/pranavsk313/AWS-Lightsail-Mysql-Configuration/assets/122976840/6db6125b-1aa4-495f-a79d-5ee603eb4a52)


### Step 2: **Deploy MySQL Database on Amazon Lightsail**:
Follow these steps to deploy a MySQL database on Amazon Lightsail:  
    - Follow the prompts to set up the MySQL database.
    - Choose additional configurations such as database size and user credentials.
![4](https://github.com/pranavsk313/AWS-Lightsail-Mysql-Configuration/assets/122976840/7065dc12-b6e1-464c-bf33-5e4d1562d099)

![5](https://github.com/pranavsk313/AWS-Lightsail-Mysql-Configuration/assets/122976840/edf912e2-8733-4724-8761-7384a41aea8d)


### Step 3: **Add Additional Database and User**:
After deploying the database instance, add an additional database and user:
- Connect to the MySQL database using a client such as MySQL Workbench or the MySQL command-line client.
- Use SQL commands to create a new database and user with appropriate privileges.

### Step 4: **Manage MySQL Database Settings**:
 - Navigate to the "Network security" tab.
 - Configure networking settings to enable "**public access**".

![7](https://github.com/pranavsk313/AWS-Lightsail-Mysql-Configuration/assets/122976840/31901716-e0aa-4759-ac61-ce6914544bdb)

### Step 5: **Configure Additional Database Settings and Snapshots**:
- Explore the Lightsail dashboard to find options for configuring database settings such as automatic backups and maintenance windows.
- Create snapshots of your database for backup and recovery purposes.

![8 1](https://github.com/pranavsk313/AWS-Lightsail-Mysql-Configuration/assets/122976840/e6e68182-ed13-4b30-b257-4a3027f4ac61)

### Step 6. Connect to the Lightsail Ubuntu instance and install Mysql-client

```bash
sudo apt-get update -y
sudo apt install mysql-client
```

### 7. Connect Remotely from a Lightsail Ubuntu Instance
  To connect remotely from a Lightsail Ubuntu instance:
- Use the MySQL client **username and password** on the Lightsail Ubuntu instance to connect to the MySQL database.
```bash
mysql -u dbmasteruser -h <Endpoint of MYSQL> -P 3306 -p
```


```
Show databases;
```
### 5. View Database Metrics

Monitor the performance of your MySQL database by viewing database metrics:
- Navigate to the Lightsail dashboard and find the metrics section for your database instance.
- Monitor metrics such as CPU utilization, disk I/O, and database connections.
