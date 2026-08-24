# Task 3 - Deploy the Application Tier (Backend API)

| S.No | Task                                                  | Answer / Implementation                                                                                                 |
| ---: | ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
|    1 | Launch EC2 Instance in the Private Application Subnet | The **Naren App Server** was launched in the **Private Application Subnet**. Subnet ID: **`subnet-0bb4dc4133e76a9c1`**. |
|    2 | Connect Through Session Manager                       | The private EC2 instance was accessed successfully using **AWS Systems Manager Session Manager**.                       |
|    3 | Install Python 3                                      | **Python 3.14.4** was installed and verified successfully.                                                              |
|    4 | Install Flask                                         | **Flask 3.1.3** was installed successfully inside a Python virtual environment.                                         |
|    5 | Check App.md                                          | The **App.md** instructions were checked and followed for the application deployment.                                   |
|    6 | Copy app.py                                           | The **app.py** file was successfully copied and is present on the EC2 instance.                                         |
|    7 | Install Dependencies                                  | The required Flask and application dependencies were installed successfully in the virtual environment.                 |
|    8 | Run Flask Application on Port 5000                    | The Flask application was successfully started on **`0.0.0.0:5000`** using the private IP **`10.0.3.160`**.             |

## AWS Configuration Used

| Configuration      | Value                          |
| ------------------ | ------------------------------ |
| Application Server | **Naren App Server**           |
| Subnet             | **`subnet-0bb4dc4133e76a9c1`** |
| Route Table        | **Naren-App-Private-RT**       |
| Python Version     | **3.14.4**                     |
| Flask Version      | **3.1.3**                      |
| Flask Port         | **5000**                       |
| Private IP         | **10.0.3.160**                 |

## Task 3 Status

**Task 3 - Application Tier (Backend API) deployment was completed successfully on AWS EC2.**
