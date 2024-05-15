# Frappe Application README

This repository contains code for various tasks in a Frappe application.

## 1. Dashboard with Number Cards

To create a dashboard with number cards, follow these steps:

1. Create a dashboard in your Frappe application.
2. Add number cards to the dashboard.
3. Use whitelisted custom methods to fetch data and populate the number cards.

## 2. Frappe REST APIs for CRUD Operations

To create Frappe REST APIs for CRUD operations of any doctype, do the following:

1. Define REST endpoints for Create, Read, Update, and Delete operations.
2. Implement methods to handle these endpoints, utilizing Frappe's built-in functionality for data manipulation.

## 3. Script Report with Columns

To create a script report showing specific columns from a doctype, follow these steps:

1. Define a script report in your Frappe application.
2. Specify the columns to be displayed: customer name, sales order name, delivery date, item code, item name, and item quantity.
3. Implement the logic to fetch and display this data from sales orders.

## 4. Override Python Class

To override a Python class in Frappe, perform the following:

1. Identify the class you wish to override.
2. Create a custom Python file with the same class name.
3. Implement the desired changes or extensions in the custom class.

## 5. Override Whitelisted Method

To override a whitelisted method in Frappe, follow these steps:

1. Identify the whitelisted method you want to override.
2. Create a custom Python file with a method of the same name.
3. Implement the desired changes or extensions in the custom method.

## 6. API for User Management

To create APIs for user management, do the following:

1. Define REST endpoints for fetching the list of users and creating a new user.
2. Implement methods to handle these endpoints, ensuring proper authentication and authorization.

## 7. Custom Doctype with Validate Trigger

To create a new doctype with specific validation logic, proceed as follows:

1. Define a new doctype with fields for first name, last name, full name, and a checkbox.
2. Implement a validate trigger to ensure that when the checkbox is checked and first name/last name are filled, full name is automatically set to the concatenation of first name and last name.

## Technologies Used

- Frappe
- Docker


## Prerequisites

Before running this project, ensure you have the following installed:

- #### Docker Desktop (Docker)
    Docker Desktop is a one-click-install application for your Mac, Linux, or Windows environment that lets you build, share, and run containerized applications and microservices.It provides a straightforward GUI (Graphical User Interface) that lets you manage your containers, applications, and images directly from your machine. Docker Desktop reduces the time spent on complex setups so you can focus on writing code. It takes care of port mappings, file system concerns, and other default settings, and is regularly updated with bug fixes and security updates.To Install Docker Desktop <a href="https://docs.docker.com/desktop/" alt="not found">Click Here</a>

- #### Frappe
    Frappe, pronounced fra-pay, is a full stack, batteries-included, web framework written in Python and Javascript with MariaDB as the database. It is the framework which powers ERPNext, is pretty generic and can be used to build database driven apps. To install latest version <a href="https://frappeframework.com/docs/user/en/introduction" alt="not found">Click Here</a>


## Installation
1. Install Docker desktop and open command prompt.
2. Inside command promt type this command
   ```bash
   docker pull ubuntu:22.04
   docker run -dt --name bench -p 8000:8000 ubuntu:22.04 /bin/bash
   ```
4. Next setup frappe framework, to setup <a href="https://wiki.nestorbird.com/wiki/install-frappe-v15">Click here</a>
5. Navigate to **Customization > DocType**
6. Create a new DocType named "Student".
7. Add the specified fields according to the provided instructions.
## Usage
1. open bench directory and inside that enable developer mode -
 ```bash
bench set-config -g developer_mode 1
  ```
2. start postgres service by running this command
   ```bash
   sudo service postgresql start
   ```
3. Start Bench with 2 commands
   ```bash
   bench use your_bench_name
   bench start
   ```
1. Navigate to the list view of the Customer Doctype.
2. Click on the "Export" button to trigger the export functionality.
3. Once the export is complete, the system will generate a CSV file containing the specified customer and address data.  

## Implementation Steps

To implement this functionality, follow these steps:

1. **Modify Customer Doctype:**
   - Add a button named "Export" to the list view of the Customer Doctype.

2. **Backend Logic:**
   - Implement backend logic to handle the button click event.
   - Fetch the required data from the database, including the specified fields from both Customer and Address doctypes.

3. **CSV File Generation:**
   - Generate a CSV file dynamically, populating it with the fetched data.

4. **Error Handling:**
   - Handle any error cases or exceptions that may occur during the export process to ensure a smooth user experience.

