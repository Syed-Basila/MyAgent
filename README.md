# 💼 My AI Career Agent — Syed Basila

An **AI-powered personal career representative** built with **CrewAI**, **Gemini API**, and **Gradio**.  
This chatbot reads your LinkedIn profile (`Profile.pdf`) and summary (`summary.txt`), then speaks naturally as **you** — representing your professional background, skills, and projects.  
It can even send emails automatically when someone wants to connect or asks a question you can’t answer.

---

## 🚀 Features

- 🧠 Reads your **LinkedIn Profile (PDF)** and **Career Summary (TXT)**.  
- 💬 Speaks in **first-person**, just like a real conversation.  
- 📩 Sends **email notifications** for:
  - New contact or hiring interest.  
  - Unanswered questions.  
- ⚙️ Powered by **Gemini API (Google AI)**.  
- 🌐 Deployable for **free** using **Gradio on Hugging Face Spaces**.

---

## 🧰 Tech Stack

- **Python 3.10+**
- [CrewAI](https://github.com/joaomdmoura/crewAI)
- [Gradio](https://gradio.app/)
- [pypdf](https://pypi.org/project/pypdf/)
- [Gemini API (Google AI)](https://ai.google.dev/)
- **Gmail SMTP** (for email notifications)

---

## 📂 Project Structure

My_Agent/
│
├── app.py # Main application file
├── Profile.pdf # Your LinkedIn profile PDF export
├── summary.txt # Your short professional summary
├── requirements.txt # Dependencies list
└── README.md # Project documentation



---

## ⚙️ Setup Instructions

### 1.Clone the Repository

```bash
git clone https://github.com/<your-username>/My_Agent_Clone.git
cd My_Agent_Clone

```
### 2.Add Your Files

Place your personal files inside the project folder:

Profile.pdf → Your LinkedIn or portfolio PDF

summary.txt → Short text summary about you

### 3.Create requirements.txt
gradio
crewai
pypdf


Then install dependencies:

pip install -r requirements.txt

### 4️. Configure Environment Variables

When you run the app, it will prompt you for:

Gemini API Key → Get from Google AI Studio

Gmail App Password → Create one at Google App Passwords

Alternatively, set them manually:

export GEMINI_API_KEY="your_gemini_api_key"
export GMAIL_APP_PASSWORD="your_gmail_app_password"
export GMAIL_USER="your_email@gmail.com"

### 5️.Run Locally
python app.py


You’ll see something like:

Running on local URL:  http://127.0.0.1:7860


Open it in your browser to chat with your AI career agent!

☁️ Deploy for Free on Hugging Face Spaces

Go to Hugging Face Spaces

Create a new Space

Choose:

SDK → Gradio

Runtime → Python 3.10+

Hardware → CPU-basic (free)

Upload these files:

app.py

Profile.pdf

summary.txt

requirements.txt

README.md

In Settings → Variables, add:

GEMINI_API_KEY=your_gemini_api_key
GMAIL_APP_PASSWORD=your_gmail_app_password
GMAIL_USER=your_email@gmail.com


Click Deploy

✅ That’s it — your chatbot will be live, 24/7, and free!

🧠 How It Works

parse_pdf() extracts text from your LinkedIn PDF.

The CrewAI Agent uses the text and summary to form your professional backstory.

The Gradio Chat Interface enables natural, first-person chat.

The send_email_tool() triggers Gmail notifications when:

A user shares contact info → “New Contact” email

A question can’t be answered → “Unanswered Question” email

📧 Email Notification Rules
1. New Contact

If someone wants to connect or hire you:

Subject: New Contact: <Name>
Message: Includes name, email, and short chat summary.

2. Unanswered Question

If the AI can’t answer:

Subject: Unanswered Question
Message: Includes the exact question and conversation summary.

💾 Memory in CrewAI

CrewAI can retain conversation memory using persistent storage.

CHROMA_OPENAI_KEY=your_key_here


This allows your AI to recall past interactions intelligently.


###Example User Prompts

“Tell me about your experience.”

“What projects have you worked on?”

“What are your key skills?”

“Can we collaborate on a project?”

“How can I contact you?”
