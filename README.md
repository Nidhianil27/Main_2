# Digital Marketplace for Byproduct Management ♻️

An AI-powered digital marketplace that connects buyers and sellers of industrial byproducts and recyclable materials, promoting material reuse, recycling, and sustainable waste management.

## 📌 Project Overview

The platform combines a digital marketplace with Artificial Intelligence and Machine Learning to help users identify waste materials, discover relevant byproduct advertisements, and receive intelligent recycling guidance.

The system integrates:

- Deep Learning for waste image classification
- LightGBM for advertisement recommendations
- RAG (Retrieval-Augmented Generation) for recycling knowledge retrieval
- Llama LLM for generating structured material insights
- Buyer–seller communication
- JWT-based authentication

## 🤖 AI & Machine Learning Components

### 1. Waste Image Classification

When a seller uploads an image of a waste material, the image is processed by the ML API and classified into categories such as:

- Plastic
- Paper
- Glass
- Metal
- Cardboard
- Trash

Multiple deep learning models were evaluated, including:

- ResNet50
- EfficientNet
- MobileNetV2

Based on the performance obtained on the project dataset, **MobileNetV2** was selected for waste classification.

### 2. Recommendation System

The platform uses **LightGBM** to recommend relevant advertisements to users.

Recommendations are based on factors such as:

- User search behaviour
- Product/material category matching
- Advertisement relevance

### 3. RAG + Llama

The system provides intelligent recycling guidance using **Retrieval-Augmented Generation (RAG)** integrated with a Llama-based Large Language Model.

After identifying the waste material:

1. The system identifies the material category.
2. RAG retrieves relevant information from a local knowledge base.
3. Retrieved information may include recycling methods, industries using the material, market price information, eco-friendly tips, and government guidelines.
4. The Llama model generates structured and user-friendly material insights.

## ♻️ Recycling Information

The system can provide information such as:

- Material description
- Recycling steps
- Industries using the material
- Approximate market price
- Eco-friendly disposal tips
- Government guidelines and regulations

## 🛒 Marketplace

The application provides a marketplace where buyers and sellers can interact around recyclable and industrial byproduct materials.

### Key Features

- Seller advertisement creation
- Product/byproduct listings
- Waste material identification
- AI-powered recommendations
- Recycling information
- Buyer–seller messaging
- User authentication

## 🏗️ Technology Stack

| Technology | Purpose |
|------------|---------|
| React | Frontend |
| Node.js | Backend |
| Express.js | Backend API |
| MongoDB | Database |
| Flask | Machine Learning API |
| MobileNetV2 | Waste image classification |
| LightGBM | Recommendation system |
| RAG | Knowledge retrieval |
| Llama | Natural language generation |
| JWT | Authentication |

## 🔄 AI Pipeline


Waste Image
     ↓
MobileNetV2
     ↓
Material Classification
     ↓
 ┌───────────────┬──────────────────┐
 ↓               ↓                  ↓
RAG          LightGBM          Marketplace
 ↓               ↓
Knowledge     Advertisement
Retrieval     Recommendation
 ↓
Llama LLM
 ↓
Structured Material
Insights
