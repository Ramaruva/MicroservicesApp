# Microservices E-Commerce Platform

This project demonstrates key microservices architecture principles using a simple e-commerce system, split into two independently running services: an Admin app and a Main app.

## 🧱 Architecture Overview

- **Admin App (Django)**: Manages product creation, updates, deletions, and user IDs for likes.
- **Main App (Flask)**: Displays products and allows users to "like" them.

## 🔗 Communication Between Services

- **RabbitMQ** (via `pika`) is used for event-driven messaging (product create/update/delete, likes).
- **Internal APIs** are used to fetch shared data (e.g., random user ID from Admin service).

## 🚀 Technologies Used

- **Backend**: Django, Flask, MySQL
- **Frontend**: React (TypeScript)
- **Messaging**: RabbitMQ
- **Containerization**: Docker, Docker Compose

## 📦 How to Run

1. Make sure Docker and Docker Compose are installed.
2. Clone the repository.
3. Run the following command:
    ```bash
    docker-compose up --build
    ```

This will start:
- Django Admin service
- Flask Main service
- Two MySQL databases
- RabbitMQ broker

## 📚 Features Demonstrated

- Microservices separation of concerns
- Asynchronous inter-service communication with RabbitMQ
- Independent scaling and deployment using Docker
- Modular front-end with React + TypeScript

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.


