AI Soul Counselor
-
AI Soul Counselor is a production-grade, backend-first AI system that creates a personalized AI companion for each user, combining Retrieval-Augmented Generation (RAG), long-term memory, and configurable personality profiles.Each user interacts with a private AI Soul that evolves over time through stored memory and personalized prompt injection.

Problem Statement
-
Long term context is critical for individuals looking for AI assisted coaching or counseling. This long term ontext relates to recurring concerns and worries, established goals and objectives, and a user's customized preferences. Most chat systems of LLMs operate only on a session basis without any saved information. As a result, those chat systems cannot allow for secure integration of user emotional context from previous chats and therefore hinder progress through consecutive conversations. 

AI Soul Counselor was created to solve this exact problem 
- 
+ Structured long term conversation memory
+ Deterministic personality enforcement
+ Strict per-user data isolation

Core Capabilites 
+ Per-user AI Soul with independent memory evolution
+ Retrieval-Augmented Generation powered by OpenAI embeddings
+ Private ChromaDB vector stores per account
+ JWT-authenticated API with OAuth2 Bearer security
+ Password hasing and protected route enforcement
+ Conversation History in PostSQL Lite
+ Dockerized deployment for cloud platforms
+ FastAPI architecture

RAG with Per-User Memory Isolation
-
All conversations are stored in a relational database and mirrored into ChromaDB as embeddings. Retrieval is only executed with authenticated user scope, which ensures privacy and Independent companions.

Chat Flow
-
1) User authentication
2) Message saved to SQL database
3) Embedding generated and stored
4) Relevant memories retrieved
5) Prompt constructed using:
   + persisted personality settings
   + Retrieved Historical context
   + Current user input
6) LLM generates response
7) Response stored and returned

Backend Archeticture
![IMG_3580](https://github.com/user-attachments/assets/61f5830e-c25d-44e4-9e5d-311f283aa435)


Design Priciples 
-
+ Modular routers with dependency layer security
+ SQLAchemy ORM and Alembic migrations
+ Service oriented AI integration
+ Extensible OpenAPI schema

Technology Stack
-
Backend
-
+ FastAPI
+ SQLAlchemy
+ Alembic
+ Pydantic
+ Uvicorn

AI/ML
-
+ Langchain
+ OpenAI
+ ChromaDB
+ Vector embeddings & RAG

Security
-
+ OAuth2 Bearer JWT
+ Protected routes
+ Paswword Hashing

Deployment
- 
+ Containerized with Docker
+ Hosted on Render Web Service
+ Enviornment configured with PostgreSQL Lite and ChromaDB
+ Live API accessible at: https://ai-soul-counsler.onrender.com/

API Documentation
-
The FastAPI backend provides an interactive Swagger UI for live endpoint testing at /docs. Authentication is supported directly in Swagger using JWT Bearer tokens.


  








