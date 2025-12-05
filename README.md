# 🚀 Multi-Agent AI Marketing Automation Platform

> **An autonomous, role-based multi-agent system built with CrewAI that performs market research, SEO optimization, and content generation for product marketing campaigns.**

This project demonstrates how **Agentic AI + multi-agent collaboration** can automate complex business workflows end-to-end. Specialized agents interact using tools, reasoning chains, and structured task orchestration to deliver publish-ready marketing assets.

---

## 🧠 Key Features

✅ **True Multi-Agent System** — 4 specialized AI agents collaborate
✅ **Role-Based Orchestration** using **CrewAI framework**
✅ **Agent tool use** (web search, website scraping, reading/writing files)
✅ **ReAct-style reasoning & planning**
✅ **Dynamic prompting via YAML configuration**
✅ **Structured outputs** using Pydantic schemas
✅ **Fully automated marketing pipelines**

---

## 👥 Crew Architecture

### 🧑‍🍳 Agents

| Agent                           | Responsibility                                              |
| ------------------------------- | ----------------------------------------------------------- |
| **Marketing Head**              | Conducts market research and builds the marketing strategy  |
| **SEO Specialist**              | Finds trending keywords and optimizes content for discovery |
| **Social Media Content Writer** | Produces LinkedIn, Twitter, Instagram & Facebook drafts     |
| **Blog Content Writer**         | Writes long-form SEO-driven blog content                    |

Each agent has:

* A defined **role**
* Clear **goal**
* Contextual **backstory**
* Access to specialized tools
* Autonomous decision‐making abilities

---

### 🔄 Workflow

```text
User Input (Product Details)
        ↓
Marketing Head → Market Research + Strategy
        ↓
SEO Specialist → Keyword Analysis & Optimization
        ↓
Writers → Blog + Social Media Content
        ↓
File Tools → Write structured outputs to disk
```

---

## 🛠 Tools Used

CrewAI built-in and custom tools power the agents:

| Tool                  | Purpose                                      |
| --------------------- | -------------------------------------------- |
| **SerperDevTool**     | Real-time web search (Google SERP)           |
| **ScrapeWebsiteTool** | Website content extraction                   |
| **FileReadTool**      | Reads local working documents                |
| **FileWriteTool**     | Writes generated outputs to disk             |
| **DirectoryReadTool** | Scans project folders for existing resources |

---

## ⚙️ Technology Stack

* **Python 3.10+**
* **CrewAI**
* **Gemini LLM** *(can be swapped with OpenAI, Claude, etc.)*
* **Serper API** (Google search)
* **YAML** prompt configuration
* **Pydantic** for structured outputs

---

---

## 📂 Project Structure

```text
multi-agent-marketing-automation/
│
├── crew.py                     # CrewAI orchestration logic
│
├── config/
│   ├── agents.yaml             # Agent role, goals & prompts
│   └── tasks.yaml              # Task descriptions & outputs
│
├── tools/
│   └── custom_tools.py         # Optional custom tools
│
├── resources/
│   └── drafts/                 # Agent-generated outputs
│
├── .env                        # API keys
├── requirements.txt
└── README.md
```

---

---

## 🧪 Sample Outputs

All generated content is saved locally:

```text
resources/drafts/
│
├── content_calendar.json
├── marketing_strategy.txt
├── linkedin_post.txt
├── instagram_reel.txt
├── facebook_post.txt
├── blog_draft.txt
├── competitor_analysis.txt
└── seo_keywords.txt
```

---

## 📝 Example Outputs

### 📅 Content Calendar

* Post schedules with dates and platforms
* Topics aligned with target demographics

---

### 📱 Social Mass Communication Drafts

LinkedIn, Twitter, Facebook & Instagram-ready posts auto-written from research data.

---

### 📰 SEO Blog

A keyword-optimized article:

* Competitive positioning
* Trend awareness
* Conversion-oriented calls to action

---

### 🔎 SEO Keyword Report

Hot keywords from real search trends:

```json
[
  "excel automation AI",
  "GPT Excel plugins",
  "zapier competitor tool",
  "microsoft copilot alternatives",
  "sheets automation SaaS"
]
```

---

---

## 🔐 Setup Instructions

---

### ✅ Step 1 — Clone Repo

```bash
git clone https://github.com/IrriDileepKumar/Multi-Agent-Marketing-Automation-System-using-CrewAI.git
cd multi-agent-marketing-automation
```

---

### ✅ Step 2 — Install Dependencies

Using pip:

```bash
pip install -r requirements.txt
```

Or using `uv`:

```bash
uv add crewai crewai-tools python-dotenv pydantic
```

---

### ✅ Step 3 — Create `.env` file

```env
GOOGLE_API_KEY=YOUR_GEMINI_API_KEY
SERPER_API_KEY=YOUR_SERPER_API_KEY
```

---

### ✅ Step 4 — Run the Crew

```bash
python crew.py
```

---

### ✅ Output

After execution completes:

📁 Go to:

```text
/resources/drafts/
```

All generated content files will be available there.

---

---

## 🧩 Customization

---

### 🔹 Change Agent Prompts

Edit:

```yaml
config/agents.yaml
```

Example:

```yaml
seo_specialist:
  role: SEO Specialist
  goal: Identify trending keywords and maximize search visibility
```

---

### 🔹 Change Tasks

Edit:

```yaml
config/tasks.yaml
```

Example:

```yaml
blog_task:
  description: Create a 1500-word SEO blog about {{product_name}}
```

---

### 🔹 Change LLM

Inside YAML:

```yaml
llm: gemini
```

Swap to:

```yaml
llm: openai
llm_model: gpt-4-turbo
```

---

---

## 🧠 Advanced Features

---

### ✅ Reasoning Mode

Activates planning + reflection:

```python
reasoning = True
planning = True
```

---

### ✅ Memory Support

Enable persistent agent memory:

```python
memory = True
embedder = "google"
```

---

### ✅ Structured Outputs

Using a Pydantic schema ensures JSON-safe outputs:

```python
class Content(BaseModel):
    content_type: str
    topic: str
    target_audience: str
    content: str
```

---

---

## 📈 Use Cases

✅ Marketing strategy automation
✅ SaaS content generation
✅ SEO optimization pipelines
✅ Competitor analysis reporting
✅ Social media mass content production
✅ Startup launch promotions

---

---

## 🎯 Resume Bullet

> **Multi-Agent AI Marketing Automation Platform | CrewAI**
>
> * Built a **4-agent autonomous marketing workforce** using CrewAI
> * Integrated real-time **search, scraping, and workflow orchestration tools**
> * Enabled **ReAct reasoning, YAML prompt configuration, and memory pipelines**
> * Automatically generated SEO blogs, social media posts, and competitor insights

---

---

## 🌱 Learning Highlights

This project demonstrates:

* End-to-end **agentic AI architecture**
* Task dependency flows
* Tool selection and structured agent collaboration
* Autonomous planning and execution

---

---

## 🛡️ Disclaimer

This project is for educational and demonstration purposes using public LLM APIs.
It does not perform posting automation or data scraping on protected content sources.

---

---

## ⭐ Contributors

**Dileep Kumar Irri**
ML Engineer | AI Researcher
Specialized in Agentic AI, Computer Vision, and Multi-modal Systems

---

---

## 🌟 Star the Repo

If you find this useful or inspiring:

> ⭐ **Leave a star — it helps a lot!**

---

---

## 📣 Contact

📧 `dileepkumarirri0@gmail.com`
💼 LinkedIn: `https://www.linkedin.com/in/dk-dileep/`
🌐 GitHub: `ghttps://github.com/IrriDileepKumar`

---

---

## ✅ Final Notes

This project highlights **modern AI engineering practices** combining:

* Multi-agent intelligence
* Real-time data access
* Structured automation
* Tool-augmented reasoning

**Perfect for demonstrating industry-grade Agentic AI skills.**

---

---

## 🚀 Happy Building!

*"The future of AI engineering is collaborative — agent teams, not single prompts.”*
