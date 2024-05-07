# Vendor-management-system

Develop a Vendor Management System using Django and Django REST Framework. This
system will handle vendor profiles, track purchase orders, and calculate vendor performance
metrics


## Installation

# 1. Clone the repository:
   bash:  
   git clone https://github.com/Aaditya110711/vendor-management-system.git  
   cd project-directory 

# 2.Create a virtual environment:
python -m venv venv  
source venv/bin/activate  # For Linux/Mac  
venv\Scripts\activate     # For Windows  

# 3.Install dependencies:
pip install -r requirements.txt  

# 4.Database setup:
python manage.py makemigrations  
python manage.py migrate  

## Usage
# 1.Start the server:
python manage.py runserver  

# 2.Access API endpoints:

## Access token  
- '/gettoken/' #provide username and password in json eg. { "username":"username","password":"PWD" }  
- I used Postman to test API  
- Once Token is created or received provide it to HEADER  with key as Authorization (eg. key : Authorization) and value as token <received-token>    .


## API Endpoints

**Vendor Profile Management**

| Endpoint               | Method      | Description                           |
| ---------------------- | ----------- | ------------------------------------- |
| `/vendors/`      | POST        | Create a new vendor.                  |
| `/vendors/`      | GET         | List all vendors.                     |
| `/vendors/{id}/` | GET         | Retrieve a specific vendor's details. |
| `/vendors/{id}/` | PUT         | Update a vendor's details.            |
| `/vendors/{id}/` | DELETE      | Delete a vendor.                      |

**Purchase Order Tracking**

| Endpoint                                  | Method       | Description                                    |
| ----------------------------------------- | ------------ | ---------------------------------------------- |
| `/purchase_orders/`                 | POST         | Create a purchase order.                       |
| `/purchase_orders/`                 | GET          | List all purchase orders.                      |
| `/purchase_orders/{id}/`            | GET          | Retrieve details of a specific purchase order. |
| `/purchase_orders/{id}/`            | PUT          | Update a purchase order.                       |
| `/purchase_orders/{id}/`            | DELETE       | Delete a purchase order.                       |
| `/purchase_orders/{id}/acknowledge` | PUT  | Acknowledge a purchase order.                  |

**Vendor Performance Evaluation**

| Endpoint                                  | Method | Description                              |
| ----------------------------------------- | ------ | ---------------------------------------- |
| `/vendors/{id}/performance`         | GET    | Retrieve a vendor's performance metrics. |

**Historical Performance API**

| Endpoint                                  | Method | Description                              |
| ----------------------------------------- | ------ | ---------------------------------------- |
| `/vendor/historical_performance`         | GET    | List historical performance for all. |
| `/vendor/historical_performance/{id}/`         | GET    | Retrieve historical performance for a specific vendor. |


