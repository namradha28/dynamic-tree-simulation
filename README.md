# dynamic-tr# 🌳 Dynamic Tree Simulation – Interactive Number Game

An interactive Dynamic Binary Search Tree (BST) Simulation Engine built using FastAPI + D3.js, containerized with Docker and deployed on Hugging Face Spaces.

This project allows users to dynamically insert and search numbers while visualizing the tree structure in real time.

---

## 📌 Project Overview

The Dynamic Tree Simulation project visualizes how Binary Search Trees work in real-time.

Users can:

- ➕ Insert numbers
- 🔍 Search numbers
- 🌳 View dynamic tree structure
- ⚡ Experience instant UI updates

The backend processes tree logic, while the frontend renders the structure using D3.js.

---

## 🏗️ Architecture

Frontend (HTML + CSS + JS + D3.js)
        ↓
FastAPI Backend
        ↓
Dynamic BST Engine (Python)

---

## ⚙️ Tech Stack

Backend:
- FastAPI
- Uvicorn
- Python 3.10

Frontend:
- HTML
- CSS
- JavaScript
- D3.js (CDN)

Deployment:
- Docker
- Hugging Face Spaces

---

## 📂 Project Structure

.
├── app.py
├── tree.py
├── requirements.txt
├── Dockerfile
└── static/
    └── index.html

---

## 🔌 API Endpoints

POST   /insert/{value}   → Insert number into tree  
GET    /search/{value}   → Search number in tree  
GET    /tree             → Get full tree structure  

---

## 🧠 How It Works

Insert Operation:
- Adds number to BST
- Maintains left < root < right property

Search Operation:
- Recursively traverses tree
- Returns true/false

Visualization:
- Backend converts tree to dictionary format
- D3.js renders hierarchical layout
- UI updates automatically

---

## 🖥️ Running Locally

1. Clone Repository

git clone https://github.com/YOUR_USERNAME/dynamic-tree.git  
cd dynamic-tree  

2. Install Dependencies

pip install -r requirements.txt  

3. Run Server

uvicorn app:app --reload --port 8002  

4. Open Browser

http://127.0.0.1:8002  

---

## 📦 requirements.txt

fastapi==0.110.0  
uvicorn[standard]==0.27.1  

---

## 🐳 Dockerfile

FROM python:3.10-slim  

WORKDIR /app  

COPY requirements.txt .  

RUN pip install --no-cache-dir -r requirements.txt  

COPY . .  

EXPOSE 7860  

CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "7860"]  

---

## 🌍 Deploying to Hugging Face Spaces

1. Create new Space  
2. Select Docker SDK  
3. Upload:
   - app.py
   - tree.py
   - requirements.txt
   - Dockerfile
   - static folder  
4. Wait for build  
5. Access live link  

---

## 🎯 Key Features

- Real-time BST simulation  
- Interactive UI  
- REST API architecture  
- Docker containerization  
- Cloud deployment ready  

---

## 💡 Future Improvements

- AVL Self-Balancing Tree  
- Delete Node Functionality  
- Score-Based Game Mode  
- Multiplayer Support  
- WebSocket Real-Time Updates  

---

## 🎤 Interview Explanation (PSI Method)

Problem:
Understanding dynamic tree operations is difficult without visualization.

Solution:
Built a full-stack interactive BST simulation using FastAPI and D3.js.

Impact:
Enables real-time algorithm visualization and improves understanding of tree data structures.

---
