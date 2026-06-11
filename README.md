[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/cTz6p1BO)

# Prompt Engineering, RAG, and Fine-Tuning for Medical Policy Assistant

## Overview

This project demonstrates three core Generative AI techniques:

1. Prompt Engineering
2. Retrieval-Augmented Generation (RAG)
3. Parameter-Efficient Fine-Tuning (LoRA)

The system is designed as a Medical Policy Assistant capable of answering questions related to healthcare company policies such as appointment scheduling, prescriptions, consultations, and patient services.

---

## Objectives

* Understand prompt-based querying with Large Language Models.
* Build a Retrieval-Augmented Generation (RAG) pipeline using LangChain and FAISS.
* Fine-tune a Small Language Model using LoRA.
* Compare prompt engineering, RAG, and fine-tuning approaches.

---

## Technologies Used

### LLM Providers

* Groq API
* Llama 3.3 70B Versatile

### RAG Components

* LangChain
* FAISS Vector Database
* Sentence Transformers
* HuggingFace Embeddings

### Fine-Tuning Components

* TinyLlama 1.1B Chat
* PEFT (LoRA)
* Transformers
* BitsAndBytes
* Accelerate
* Datasets

### Programming Language

* Python

### Environment

* Google Colab

---

## Project Workflow

### 1. Prompt Engineering

The first stage uses direct prompting with a Large Language Model through the Groq API.

Workflow:

User Query
→ Llama Model
→ Generated Response

This method relies solely on the model's existing knowledge and prompt instructions.

---

### 2. Retrieval-Augmented Generation (RAG)

A medical company policy document is loaded and indexed.

Steps:

1. Load policy documents.
2. Generate embeddings using:

   * all-MiniLM-L6-v2
3. Store embeddings in FAISS.
4. Retrieve relevant information using similarity search.
5. Pass retrieved context to the LLM.
6. Generate accurate responses.

Workflow:

User Query
→ Vector Search
→ Relevant Documents
→ LLM
→ Answer

---

### 3. LoRA Fine-Tuning

TinyLlama is fine-tuned on custom medical policy question-answer pairs.

Fine-Tuning Features:

* PEFT (Parameter Efficient Fine Tuning)
* LoRA Adapters
* Quantized Training
* Reduced GPU Memory Usage

Workflow:

Custom Dataset
→ Tokenization
→ LoRA Configuration
→ Training
→ Fine-Tuned Model

---

## Dataset

The project uses custom medical company policy data covering:

* Appointment Policies
* Prescription Guidelines
* Consultation Rules
* Patient Services
* Scheduling Procedures

---

## Sample Questions

Examples:

* What is the Appointment Policy?
* How can patients book appointments?
* What is the Prescription Policy?
* Can appointments be rescheduled?

---

## Learning Outcomes

Through this project, the following concepts were explored:

* Prompt Engineering
* Embedding Generation
* Semantic Search
* Vector Databases
* Retrieval-Augmented Generation
* LoRA Fine-Tuning
* Hugging Face Transformers
* PEFT
* Medical Domain Question Answering

---

## Future Improvements

* Deploy as a web application.
* Add conversational memory.
* Use larger healthcare datasets.
* Implement Hybrid Search.
* Integrate local LLMs using Ollama.
* Build an MCP-enabled agent architecture.

---

## Author

Nivash M

Department of Computer Science and Engineering

Generative AI Learning Project
