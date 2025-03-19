# Booking Analytics API

This project provides a FastAPI-based analytics and Q&A system for hotel bookings, including revenue trends, cancellation rates, geographical distribution, and lead time analysis. The system integrates an open-source LLM with Retrieval-Augmented Generation (RAG) and is containerized using Docker.

## Features
- Revenue trends over time
- Cancellation rate analysis
- Geographical distribution of users
- Booking lead time distribution
- Natural language Q&A using an open-source LLM
- Deployed using Docker

## Installation & Setup

### Prerequisites
- Docker installed on your system
- Git installed on your system

### Clone the Repository
```sh
git clone https://github.com/rushi-ace-01/booking-analytics-api.git
cd booking-analytics-api
```

### Build and Run the Docker Container
```sh
docker build -t booking-api .
docker run -p 8000:8000 booking-api
```

### Access the API
The API will be available at:
```
http://localhost:8000/docs
```

## API Endpoints

### 1. Analytics Reports
#### `POST /analytics`
Request Body:
```json
{
  "report_type": "revenue_trends"
}
```
Response:
```json
{
  "revenue_trend_plot": "<base64-encoded-image>"
}
```

### 2. Q&A System
#### `POST /ask`
Request Body:
```json
{
  "question": "What was the highest revenue month?"
}
```
Response:
```json
{
  "answer": "The highest revenue month was August 2023."
}
```

### 3. Performance Evaluation
#### `POST /evaluate`
Evaluates Q&A accuracy and API performance.

## Implementation Choices & Challenges
- Used FastAPI for fast and asynchronous API handling.
- FAISS and SciPy used for efficient vector search.
- Llama 2 chosen for Q&A system due to its lightweight yet powerful performance.
- Docker containerization for easy deployment.

## Contribution
Feel free to fork the repo and submit pull requests!

## License
MIT License

