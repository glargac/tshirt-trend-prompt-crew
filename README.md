# 👕 Trend-to-Prompt Multi-Agent System

An end-to-end multi-agent AI pipeline built with **CrewAI** and **LLMs** (Google Gemini / Ollama) that automates fashion trend analysis and generates technical image generation prompts for **Leonardo.ai**.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![CrewAI](https://img.shields.io/badge/Framework-CrewAI-FF4B4B?style=flat)
![Google Gemini](https://img.shields.io/badge/LLM-Gemini_1.5_Flash-8E44AD?style=flat&logo=google&logoColor=white)
![Jupyter](https://img.shields.io/badge/Environment-Jupyter_Notebook-F37626?style=flat&logo=jupyter&logoColor=white)

---

## 📌 Business Overview

In the fast-paced e-commerce and print-on-demand (POD) industry, turning market trends into ready-to-print designs quickly is crucial. This project implements an automated multi-agent architecture where specialized AI agents collaborate sequentially to convert high-level niche trends into optimized, technical prompts ready for image generation tools like **Leonardo.ai**.

---

## 🏗️ Architecture & Workflow

This pipeline operates sequentially across two specialized AI agents:

1. **Input Theme:** `Raw Trend / Niche Concept`
2. **🕵️ Trend Researcher Agent:** Analyzes visual styles, color palettes, and graphic components.
3. **🎨 Prompt Engineer Agent:** Converts structured analysis into technical keywords (vectors, isolations, lighting).
4. **Output Result:** `Optimized Leonardo.ai Technical Prompt`

---

### Agent Roles & Key Responsibilities

* **Trend Researcher Agent:** Analyzes raw market themes or seasonal events to extract core graphic components, color harmony, and aesthetic styles suited for streetwear and dropshipping.
* **Prompt Engineer Agent:** Takes the structured researcher's output and formats it into strict technical prompts in English, enforcing parameters such as flat design, vector illustrations, isolated white backgrounds, and rendering quality keywords.

---

## 🚀 Tech Stack

* **Orchestration:** CrewAI
* **LLM Engine:** Google Gemini (`gemini-1.5-flash`) / Local fallback with Ollama (`llama3.2:1b`)
* **Development Environment:** VS Code + Jupyter Notebooks (`.ipynb`)
* **Target Platform:** Leonardo.ai
* **Language:** Python 3.10+

---

## 💻 Getting Started

### 1. Clone the Repository

bash
git clone https://github.com/glargac/tshirt-trend-prompt-crew.git
cd tshirt-trend-prompt-crew

### 2. Install Dependencies

bash
pip install crewai langchain-google-genai

### 3. Configure API Key
Set up your Google Gemini API key inside your environment or directly within the notebook session:

python
import os
os.environ["GEMINI_API_KEY"] = "YOUR_GEMINI_API_KEY"

### 4. Run the Pipeline
Open `1_trend_to_prompt_agents.ipynb` in VS Code, choose your Python kernel, and execute the cells sequentially.

---

## 📄 Output Example

**Input Event:**
> *"Conciertos de Rock Años 80 combinados con estética de carreras de autos"*

**Generated Leonardo.ai Prompt:**
> `"T-shirt graphic design, 1980s retro rock concert aesthetic blended with vintage car racing elements, bold vector art style, isolated on pure white background, vibrant neon red and electric blue palette, crisp edges, flat screen-printing aesthetic, highly detailed, centered composition --no mockup, realistic t-shirt, shadow"`

---

## 🎯 Future Enhancements

* **LangGraph Integration:** Add complex decision-making loops and validation steps between agents.
* **RAG System:** Connect a vector database containing historical top-selling POD designs.
* **API Automation:** Integrate directly with Leonardo.ai API to automatically trigger image generation upon prompt creation.