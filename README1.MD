# 🛒 E-Commerce AI Support Chatbot

<p align="center">
  <img src="images/chatbot-banner.png" alt="E-Commerce AI Support Chatbot" width="900">
</p>

<p align="center">
  <strong>AI-Powered Customer Support System using n8n, Google Gemini, PostgreSQL, and RAG</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/n8n-Automation-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Google-Gemini-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/RAG-AI%20Search-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/AI-Agent-red?style=for-the-badge">
</p>

---

# 📖 Overview

This project is an AI-powered E-Commerce Customer Support Chatbot built using **n8n**, **Google Gemini**, **PostgreSQL**, and **Retrieval-Augmented Generation (RAG)**.

The chatbot can answer customer queries by combining:

- Company knowledge base (PDF documents)
- Order database
- Product database
- Refund database
- Support ticket database

Instead of giving generic responses, the AI retrieves real business data and provides accurate customer support similar to Flipkart, Amazon, or Shopify support systems.

---

# 🚀 Features

### 📦 Order Tracking

- Check order status
- Expected delivery date
- Order information lookup

### 💰 Refund Status

- Refund tracking
- Refund amount information
- Return status lookup

### 🛍 Product Search

- Product details
- Product descriptions
- Product pricing
- Stock availability

### 🎫 Support Ticket Creation

- Escalate unresolved issues
- Generate support tickets automatically
- Store customer complaints

### 📄 Knowledge Base (RAG)

- PDF document search
- Company FAQs
- Policies and procedures
- Context-aware responses

### 🤖 AI Agent

- Natural language understanding
- Multi-tool reasoning
- Context memory
- Human-like customer interactions

---

# 🏗️ System Architecture

```text
Customer
    │
    ▼
Chat Interface
    │
    ▼
Google Gemini AI Agent
    │
    ├── Order Lookup Tool
    │
    ├── Refund Lookup Tool
    │
    ├── Product Search Tool
    │
    ├── Ticket Creation Tool
    │
    └── PDF Knowledge Base (RAG)
                │
                ▼
        Vector Store Search
                │
                ▼
         Final AI Response
```

---

# ⚙️ Tech Stack

| Technology | Purpose |
|------------|----------|
| n8n | Workflow Automation |
| Google Gemini | AI Agent & Embeddings |
| PostgreSQL | Business Database |
| RAG | Knowledge Retrieval |
| Vector Store | Semantic Search |
| PDF Loader | Knowledge Base Ingestion |
| AI Agent | Tool Calling & Reasoning |

---

# 🗄 Database Design

## Customers

```sql
customers
```

Stores customer information.

| Column |
|----------|
| customer_id |
| name |
| email |
| phone |

---

## Products

```sql
products
```

Stores product catalog.

| Column |
|----------|
| product_id |
| name |
| description |
| price |
| stock |

---

## Orders

```sql
orders
```

Stores customer orders.

| Column |
|----------|
| order_id |
| customer_id |
| product_id |
| status |
| order_date |
| expected_delivery |

---

## Returns

```sql
returns
```

Stores refund and return requests.

| Column |
|----------|
| return_id |
| order_id |
| status |
| refund_amount |
| requested_date |

---

## Tickets

```sql
tickets
```

Stores support escalation requests.

| Column |
|----------|
| ticket_id |
| customer_message |
| issue_summary |
| status |
| created_at |

---

# 📸 Screenshots

## Workflow

![Workflow](images/workflow.png)

---

## Chatbot Interface

![Chatbot](images/chatbot.png)

---

## PostgreSQL Database

![Database](images/database.png)

---

## Vector Store

![Vector Store](images/vectorstore.png)

---

# 🔍 Example Queries

### Order Tracking

```text
Where is my order ORD12345?
```

Response:

```text
Your order ORD12345 has been shipped.

Expected Delivery:
2026-08-05
```

---

### Refund Status

```text
What is the refund status of ORD12346?
```

Response:

```text
Refund Status:
Refund Initiated

Amount:
₹699.00
```

---

### Product Search

```text
Show me wireless mouse products
```

Response:

```text
Wireless Mouse

Price: ₹699

Stock: 120 units available
```

---

### Support Escalation

```text
I want to speak with customer support.
```

Response:

```text
Support ticket created successfully.

Ticket ID:
101
```

---

# 🧠 RAG Workflow

The chatbot uses Retrieval-Augmented Generation:

1. Load PDF
2. Convert PDF into documents
3. Generate embeddings
4. Store vectors
5. Search relevant chunks
6. Pass context to Gemini
7. Generate accurate answer

---

# 🔄 n8n Workflow

```text
Read PDF
    │
    ▼
Document Loader
    │
    ▼
Gemini Embeddings
    │
    ▼
Vector Store
    │
    ▼
AI Agent
    │
    ├── PostgreSQL Tools
    └── RAG Search
```

---

# 📈 Future Improvements

- WhatsApp Integration
- Voice AI Agent
- Multi-language Support
- User Authentication
- Shipment Tracking API
- Analytics Dashboard
- CRM Integration
- Email Notifications
- Admin Panel

---

# 🎯 Skills Demonstrated

- AI Agents
- RAG Systems
- Prompt Engineering
- n8n Automation
- PostgreSQL
- Google Gemini
- Vector Databases
- Customer Support Automation
- Workflow Design
- Tool Calling

---

# 👨‍💻 Author

### Dhineshwar S

AI Automation Engineer | n8n Developer | GenAI Enthusiast

### Skills

- n8n
- Python
- PostgreSQL
- Google Gemini
- AI Agents
- RAG
- Automation

---

⭐ If you found this project useful, consider starring the repository.