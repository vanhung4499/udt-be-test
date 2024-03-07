# Section 5: Final Archictecture

## Solution

I will split the project to multiple modules, each module will be a separate project. The following is the final architecture of the project:

- Auth Module: This module will handle the authentication and authorization of the project. I will use Spring Security to implement this module. I will use JWT for authentication and use role data in jwt to authorize.
- Product Module: This module will handle the products of the project. This module will have a MongoDB database to store products data. This module will have a scheduler to synchronize products, pricing of the Agency by using third-party API. Maybe I can you ElasticSearch to store products data, because ElasticSearch is more suitable for searching text in products.
- Order Module: This module will handle the orders of the project (including cart and billing). This module will have a MySQL database to store orders data. This module will have a scheduler to send email to user when the order is created. Maybe I can use RabbitMQ to send email to user, because RabbitMQ is more suitable for sending email to user.
- Admin Module: This module will handle the admin of the project. This module will have a MySQL database to store admin data. This module will have a scheduler to send email to admin when the order is created. Maybe I can use RabbitMQ to send email to admin.

For isolating development and production environment, the project will have 2 environments: development, and production. Each environment will have its own database and its own configuration.

## CI/CD

Not yet implemented.