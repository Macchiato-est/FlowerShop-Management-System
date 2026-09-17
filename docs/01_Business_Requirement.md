# Business Requirement Document

## 1. Business Objective

The purpose of this system is to provide a web-based platform that supports flower shop operations by digitizing product management, customer ordering processes, and order management.

The system aims to:

- Provide customers with an online platform to browse flowers and place orders.
- Support administrators in managing products, categories, customers, and orders.
- Improve the efficiency of managing flower shop information compared with traditional manual processes.

## 2. Stakeholders

| Stakeholder | Description |
|---|---|
| Customer | Browse flower products, manage shopping cart, place orders, and track order status |
| Administrator | Manage products, categories, customers, and orders |
| Flower Shop Owner | Monitor and operate online sales activities |

## 3. System Scope

The system includes the following main modules:

### Customer Module

- Account registration and login
- Browse and search flower products
- View product details
- Manage shopping cart
- Place orders
- View order history


### Administrator Module

- Manage flower products
- Manage product categories
- Manage customer accounts
- Manage customer orders
- Manage website content

## 4. Functional Requirements

| ID | Actor | Requirement |
|---|---|---|
| FR-01 | Customer | Customer can register an account |
| FR-02 | Customer | Customer can login to the system |
| FR-03 | Customer | Customer can browse and search flower products |
| FR-04 | Customer | Customer can view flower product details |
| FR-05 | Customer | Customer can add products to shopping cart |
| FR-06 | Customer | Customer can place orders |
| FR-07 | Customer | Customer can view order history and order status |
| FR-08 | Administrator | Administrator can manage flower products |
| FR-09 | Administrator | Administrator can manage flower categories |
| FR-10 | Administrator | Administrator can manage customer accounts |
| FR-11 | Administrator | Administrator can manage orders and update order status |
| FR-12 | Administrator | Administrator can manage website content |
| FR-13 | System | System should validate product availability before order confirmation |

## 5. Non-functional Requirements

| ID | Category | Requirement |
|---|---|---|
| NFR-01 | Performance | The system should provide acceptable response time for common user operations |
| NFR-02 | Security | User authentication and authorization should be implemented to protect user information |
| NFR-03 | Usability | The system interface should be simple and easy for customers to use |
| NFR-04 | Reliability | The system should maintain data consistency during ordering processes |
| NFR-05 | Maintainability | The system structure should support future improvements and feature expansion |

## 6. Known Issues and Improvements

### ISSUE-001: Product Quantity Inconsistency During Order Processing

| Attribute | Description |
|---|---|
| Severity | High |
| Status | Open |

**Description:**

Multiple customers can order the same remaining product quantity before administrator confirmation.

**Impact:**

Inventory data inconsistency and incorrect order approval.

**Recommendation:**

Implement inventory reservation mechanism during checkout.
