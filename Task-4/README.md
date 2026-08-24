# Task 4 - Deploy and Configure the Database Tier

| S.No | Task | Answer / Implementation |
|---:|---|---|
| 1 | Create an Amazon RDS MySQL Instance | The **Naren Database** RDS MySQL instance was created for the Database Tier. |
| 2 | Deploy the Database in the Database Subnets | The RDS MySQL instance was deployed in the **Database Subnets** using the configured DB Subnet Group. |
| 3 | Configure Database Credentials | The database credentials were configured with the required master username and password. **The password is not included in this documentation for security.** |
| 4 | Check `DB.md` in GitHub for Instructions | The `DB.md` file in GitHub was checked and the provided database setup and SQL instructions were followed. |
| 5 | Connect DB in App EC2 Terminal | The RDS MySQL database was connected from the **Naren App Server** EC2 terminal using the RDS endpoint and configured credentials. |
| 6 | Execute the Provided SQL Commands in the Terminal | The SQL commands provided in `DB.md` were executed successfully from the App EC2 terminal. |
| 7 | Verify Connectivity from the Flask Application | The Flask application was verified for connectivity with the RDS MySQL database. |

## AWS Configuration Used

| Configuration | Value |
|---|---|
| RDS Instance Name | **Naren Database** |
| Database Engine | **MySQL** |
| DB Instance Identifier | **naren-db** |
| DB Subnet Group | **Naren DB Subnet Group** |
| VPC ID | **vpc-02ee6cb19b7fe6387** |
| Database Subnet 1 | **subnet-0dad776d0eb5fb9c6** |
| Database Subnet 2 | **subnet-03ebc86567f72a083** |
| Database Endpoint | **naren-db.c14ksuagknee.ap-south-1.rds.amazonaws.com** |
| Database Port | **3306** |
| Master Username | **admin** |
| App EC2 Server | **Naren App Server** |
| App Server Private IP | **10.0.3.160** |

## Screenshots

The following screenshots are included as proof of implementation:

1. **RDS MySQL Instance**
2. **Database Subnet Group**
3. **RDS Network and Security Configuration**
4. **MySQL Connection from App EC2 Terminal**
5. **SQL Commands and Output**
6. **Flask Application Database Connectivity**

## Task 4 Status

**Database Tier deployment and configuration completed successfully.**
