# 🧬 Multi-Agent Pharmaceutical Discovery Platform

> **AI-powered drug discovery pipeline where 5 specialized agents collaborate to discover, analyze, and validate novel drug candidates — powered by Google Gemini API.**

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.109-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org)
[![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=for-the-badge&logo=sqlite&logoColor=white)](https://sqlite.org)
[![Gemini](https://img.shields.io/badge/Google-Gemini%20API-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-3.4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [The 5 Specialized Agents](#-the-5-specialized-agents)
- [Pipeline Flow](#-pipeline-flow)
- [Key Features](#-key-features)
- [Tech Stack](#️-tech-stack)
- [Architecture](#-architecture)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [API Endpoints](#-api-endpoints)
- [Database Schema](#-database-schema)
- [Screenshots](#-screenshots)
- [How It Works](#-how-it-works)
- [Learning Outcomes](#-learning-outcomes)
- [Testing](#-testing)
- [Roadmap](#️-roadmap)
- [Disclaimer](#️-disclaimer)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)
- [Acknowledgements](#-acknowledgements)

---

## 📖 Overview

**Multi-Agent Pharmaceutical Discovery Platform** is a full-stack AI application that automates the early stages of drug discovery using a **multi-agent architecture**. Instead of relying on a single LLM call, the platform orchestrates **5 specialized AI agents**, each responsible for a distinct phase of the pharmaceutical discovery pipeline.

The platform takes a **disease name and target protein** as input and produces a **validated drug candidate** along with **complete clinical documentation** — all within minutes.

This project is designed for **educational and research purposes**, runs entirely on a **CPU-only machine**, and leverages the **Google Gemini API** for intelligent reasoning at every stage.

> 💡 **Why Multi-Agent?** Real drug discovery involves multiple scientific disciplines — chemistry, toxicology, structural biology, pharmacology, and clinical research. Each agent in this platform emulates a specialist in one of these domains, mirroring how a real pharmaceutical R&D team operates.

---

## 🎯 Problem Statement

Traditional drug discovery is:

- ⏳ **Time-consuming** — 10–15 years from concept to market
- 💰 **Expensive** — ~$2.6 billion average cost per approved drug
- ❌ **High failure rate** — ~90% of candidates fail in clinical trials
- 🧪 **Repetitive early-stage tasks** — molecule generation, toxicity screening, binding analysis

These early-stage tasks are **highly automatable** using AI agents that reason through chemical and biological constraints. This platform demonstrates how **agentic AI pipelines** can accelerate these early stages.

---

## 🤖 The 5 Specialized Agents

Each agent is an independent module with its own prompt, logic, and output schema. They execute **sequentially**, where each agent's output becomes the next agent's input.

| # | Agent | Responsibility | Input | Output |
|---|-------|----------------|-------|--------|
| 1️⃣ | **Molecule Agent** | Generates novel drug-like molecules (SMILES) for a given disease and target | Disease, target protein | 5–10 candidate SMILES + predicted properties |
| 2️⃣ | **Toxicity Agent** | Predicts toxicity (LD50, hepatotoxicity, cardiotoxicity, mutagenicity) | Candidate SMILES | Toxicity scores + Safe/Toxic verdict |
| 3️⃣ | **Protein Agent** | Predicts protein–ligand binding affinity and docking scores | Safe molecules | Binding scores + interaction residues |
| 4️⃣ | **Optimization Agent** | Improves the best candidate for better efficacy & lower toxicity | Top molecule | Optimized SMILES + modifications list |
| 5️⃣ | **Validation Agent** | Performs ADMET analysis, Lipinski's rule check, and generates clinical docs | Optimized molecule | Final verdict + clinical report |

---

## 🔄 Pipeline Flow



---

## ✨ Key Features

- 🧠 **5 Independent AI Agents** with clear separation of concerns
- 🔗 **Sequential Pipeline Orchestration** with real-time progress tracking
- 🎨 **Beautiful React UI** — dark mode, glassmorphism, Framer Motion animations
- ⚡ **Live Agent Progress** — watch each agent work in real-time
- 🧪 **Molecule Visualization** — 2D structure rendering from SMILES
- 📊 **Interactive Charts** — toxicity radar, binding affinity, optimization comparison
- 📄 **Auto-Generated Clinical Reports** — downloadable as JSON / PDF
- 💾 **SQLite Database** — zero setup, file-based, CPU-friendly
- 🔌 **RESTful API** with auto-generated Swagger docs at `/docs`
- 🖥️ **CPU-Only** — no GPU required, runs on any laptop
- 🔐 **JWT Authentication** for user sessions
- 📝 **Comprehensive Logging** — every agent action is logged
- 🧩 **Extensible** — easily add new agents to the pipeline

---

## 🛠️ Tech Stack

### Backend
| Technology | Purpose |
|-----------|---------|
| **Python 3.10+** | Core language |
| **FastAPI** | Async web framework |
| **SQLAlchemy** | ORM for SQLite |
| **Pydantic** | Data validation |
| **Google Gemini API** | LLM reasoning for agents |
| **Uvicorn** | ASGI server |
| **RDKit** | SMILES validation & molecule properties |
| **Python-JOSE** | JWT token handling |
| **Passlib** | Password hashing |

### Frontend
| Technology | Purpose |
|-----------|---------|
| **React 18** | UI framework |
| **Vite** | Build tool |
| **Tailwind CSS** | Styling |
| **Framer Motion** | Animations |
| **Recharts** | Data visualization |
| **Axios** | HTTP client |
| **React Router v6** | Routing |
| **Zustand** | State management |
| **Lucide React** | Icons |
| **React Hot Toast** | Notifications |
| **SmilesDrawer** | Molecule rendering |

### Database
| Technology | Purpose |
|-----------|---------|
| **SQLite** | Primary datastore |
| **Alembic** | Migrations (optional) |

---

## 🏗️ Architecture



---

## 🚀 Getting Started

### Prerequisites

- **Python** 3.10 or higher
- **Node.js** 18 or higher
- **Git**
- **Google Gemini API Key** → [Get one free](https://aistudio.google.com/app/apikey)

---

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/multi-agent-pharma-discovery.git
cd multi-agent-pharma-discovery


cd backend

# Create virtual environment
python -m venv venv

# Activate it
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env from example
cp .env.example .env
# Now edit .env and add your GEMINI_API_KEY

# Initialize the database
python scripts/init_db.py

# Run the server
uvicorn main:app --reload --port 8000

cd frontend

# Install dependencies
npm install

# Create .env from example
cp .env.example .env

# Run dev server
npm run dev