# LangGraph Text Processing Pipeline
I have just started my journey to learn AI-AGENTS from scratch and this is my first small and simple project for the same.
This project demonstrates a **LangGraph-based LLM workflow** that performs:

1. Text classification
2. Entity extraction (Person, Organization, Location)
3. Text summarization

The pipeline is implemented using **LangGraph**, **LangChain**, and **OpenAI** models.

---

## 📁 Project Structure

```
ai_agent_project/
├── app/ or main.py        # Your main Python script (LangGraph workflow)
├── agent_env/             # Python virtual environment (ignored by git)
├── source/                # Auto-generated dependency folder (ignored by git)
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (NOT committed)
├── .env.example           # Sample env file
├── .gitignore
└── README.md
```

---

## ⚙️ Prerequisites

* Python **3.9+** (recommended)
* macOS / Linux / Windows
* An **OpenAI API key**

Verify Python:

```bash
python3 --version
```

---

## 🧪 Setup Instructions

### 1️⃣ Clone the repository

```bash
cd ai_agent_project
```

---

### 2️⃣ Create and activate virtual environment

```bash
python3 -m venv agent_env
source agent_env/bin/activate   # macOS / Linux
```

On Windows:

```cmd
agent_env\Scripts\activate
```

---

### 3️⃣ Install dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

If `requirements.txt` is missing, install manually:

```bash
pip install langgraph langchain langchain-openai python-dotenv
```

---

### 4️⃣ Configure environment variables

Create a `.env` file at the project root:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

⚠️ **Never commit `.env` to GitHub**

---

## ▶️ Running the Project

Run the main Python file:

```bash
python app/main.py
```

---

## 🧠 What the Pipeline Does

1. **Classification Node**

   * Classifies text into: `News`, `Blog`, `Research`, or `Other`

2. **Entity Extraction Node**

   * Extracts relevant entities based on classification

3. **Summarization Node**

   * Produces a one-sentence summary

The workflow is executed sequentially using **LangGraph**.

---

## 🧪 Example Output

```text
Classification: Research
Entities: ['OpenAI', 'GPT-4', 'GPT-3']
Summary: OpenAI introduced GPT-4, a scalable and efficient multimodal AI model.
```

---

## 🔐 Notes on Cost & Quotas

* Uses `gpt-3.5-turbo` by default
* Ensure your OpenAI account has **active billing or free quota**

---

## 🛠 Troubleshooting

### OpenAI quota error

```text
openai.RateLimitError: insufficient_quota
```

✔ Check billing status
✔ Verify correct API key
✔ Confirm model availability

---

## 🚀 Next Improvements

* Add conditional branching (classification-based flow)
* Add validation / critic agents
* Convert to a true multi-agent architecture
* Add structured JSON outputs

---

## 📜 License

MIT License (or your preferred license)

---

Built with ❤️ using LangGraph, LangChain, and OpenAI
