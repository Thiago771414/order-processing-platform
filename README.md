# Food Delivery Platform – Full-Stack Monorepo
![Java](https://img.shields.io/badge/Backend-SpringBoot-green)
![React](https://img.shields.io/badge/Web-React-blue)
![React Native](https://img.shields.io/badge/Mobile-ReactNative-purple)
![Monorepo](https://img.shields.io/badge/Architecture-Monorepo-orange)

Java Spring Boot API + React Web + React Native Mobile

A full-stack food delivery platform demonstrating how a distributed system handles orders from mobile devices through backend processing and delivery workflow management.

---

<p align="center">
  <img src="https://raw.githubusercontent.com/Thiago771414/imagensProjetos/main/slices/mobile/ifood.png" width="900">
</p>

---

# Live Demo

Web interface deployed on Netlify:

https://thiagoreislimasds2.netlify.app/

⚠ Important note

The backend was originally deployed on Heroku, but Heroku discontinued the free tier.

Because of that, the cloud demo currently loads **only the frontend interface**.

The complete backend implementation and mobile application source code are fully available in this repository and the full system can be executed locally.

---

# Overview

This project simulates a **food delivery ordering system**, where users place orders through a mobile or web interface.

The system processes requests through a backend service responsible for order management and delivery queue handling.

When a delivery is completed, the order is removed from the processing queue.

The project demonstrates how a **multi-client architecture** interacts with a centralized backend service.

---

# Engineering Problem

Modern delivery platforms must handle multiple interaction layers:

• mobile ordering interfaces  
• web dashboards  
• backend order processing  
• real-time order queues  

Without a structured architecture, order management systems can suffer from:

• inconsistent order state  
• synchronization issues between clients  
• queue management problems  
• UI and API integration failures  

This project demonstrates how a backend service can coordinate orders from multiple clients.

---

# Solution

The platform implements a **three-layer architecture**:

Mobile Application  
↓  
Backend API  
↓  
Order Processing and Delivery Queue  

Users can:

• select products  
• define delivery location  
• submit orders through the mobile interface  

The backend receives the request, stores the order, and manages the delivery lifecycle.

Once a delivery is completed, the order is removed from the queue.

---

# System Architecture

```bash
Mobile App (React Native)
│
│ HTTP Request
▼
Spring Boot API
│
│ Persist Orders
▼
Database
│
│ Order Status Updates
▼
Web Dashboard (React)
```

---

# Architecture Diagram

Typical system flow:

```bash
Customer (Mobile App)
│
│ Place Order
▼
Spring Boot API
│
│ Store Order
▼
Order Queue
│
│ Delivery Completed
▼
Remove Order From Queue
```

---

# Application Interfaces

## Web Interface

Restaurant operators can visualize incoming orders through the React dashboard.

# Demo

<div align="center">


| Web Interface (React) | Product & Location (Mobile) |
| :---: | :---: |
| <a href="https://www.linkedin.com/posts/thiago-lima-2a5896166_reactnative-activity-6818886219619995648--Qql?utm_source=share&utm_medium=member_desktop&rcm=ACoAACekQx0BRU42DiOxF8SrppfeuTwD5GESrF4"><img src="https://raw.githubusercontent.com/Thiago771414/imagensProjetos/main/slices/mobile/SDS2_01.jpg" width="350"></a> | <a href="https://www.linkedin.com/posts/thiago-lima-2a5896166_java-springboot-activity-6797310232222601216-v5i-?utm_source=share&utm_medium=member_desktop&rcm=ACoAACekQx0BRU42DiOxF8SrppfeuTwD5GESrF4"><img src="https://raw.githubusercontent.com/Thiago771414/imagensProjetos/main/slices/mobile/SDS2_02.jpg" width="180"></a> <a href="https://www.linkedin.com/posts/thiago-lima-2a5896166_java-springboot-activity-6797310232222601216-v5i-?utm_source=share&utm_medium=member_desktop&rcm=ACoAACekQx0BRU42DiOxF8SrppfeuTwD5GESrF4"><img src="https://raw.githubusercontent.com/Thiago771414/imagensProjetos/main/slices/mobile/SDS2_03.jpg" width="180"></a> |
| [🌐 See web operation](https://www.linkedin.com/posts/thiago-lima-2a5896166_reactnative-activity-6818886219619995648--Qql?utm_source=share&utm_medium=member_desktop&rcm=ACoAACekQx0BRU42DiOxF8SrppfeuTwD5GESrF4) | [📱 See Mobile Operation](https://www.linkedin.com/posts/thiago-lima-2a5896166_java-springboot-activity-6797310232222601216-v5i-?utm_source=share&utm_medium=member_desktop&rcm=ACoAACekQx0BRU42DiOxF8SrppfeuTwD5GESrF4) |

**Click on the image above to watch the demonstration**

</div>

---

# Monorepo Structure

```bash
delivery-platform
│
├── backend
│ └── Spring Boot API
│
├── frontend-web
│ └── React Web Dashboard
│
├── mobile
│ └── React Native App
│
└── README.md
```

---

# Technologies Used

## Backend

Java  
Spring Boot  
REST API

## Frontend Web

React  
JavaScript  
HTML / CSS

## Mobile

React Native

---

# Running the Project Locally

Clone the repository:

```bash
git clone
```

Start the backend:

```bash
cd backend
./mvnw spring-boot:run
```
Start the web interface:

```bash
cd frontend-web
npm install
npm start
```

Run the mobile app:

```bash
cd mobile
npm install
expo start
```

---

# Engineering Value

This project demonstrates practical experience with:

• full-stack architecture design  
• monorepo organization  
• API-driven application development  
• mobile + web client integration  
• backend order processing systems  

The architecture reflects patterns used in modern delivery platforms where multiple clients interact with centralized backend services.

---

# Author

Thiago Reis Lima  
Software Engineer

LinkedIn  
```bash
https://www.linkedin.com/in/thiago-lima-2a5896166/
```
