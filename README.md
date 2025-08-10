# 🧠 profAi

![profAi logo](public/logo_dark.png)

**profAi** is your all-in-one AI-powered knowledge assistant, designed to help teams recall, organize, and interact with information seamlessly. With immersive modes, media processing, and a robust knowledge base, profAi supercharges productivity and collaboration.

---

## 🚀 Features

- **Knowledge Base:** Centralize and search your team’s knowledge.
- **Media Processor:** Extract insights from audio, video, and documents.
- **Immersive Mode (Beta):** Experience next-level interaction with your data.
- **Event Q&A:** Instantly answer questions about past events and conversations.
- **Customizable UI:** Personalize your experience with themes and avatars.
- **Chainlit & Streamlit Integration:** Modern, interactive web interfaces.

---

## 📦 Folder Structure

```
profai/
├── Home.py                # Main Streamlit app
├── pages/                 # Modular app pages
├── public/                # Static assets (images, CSS, JS)
├── archive/               # Legacy or archived scripts
├── .chainlit/             # Chainlit configuration
├── .streamlit/            # Streamlit configuration
├── startup_scripts/       # Service scripts for deployment
├── requirements.txt       # Python dependencies
├── README.md              # Project documentation
└── ...
```

---

## ⚡️ Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/profai.git
   cd profai
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   - Copy `.env.sample` to `.env` and fill in your secrets.

5. **Run the app**
   ```bash
   streamlit run Home.py
   ```
   The app will open at [http://localhost:8501](http://localhost:8501).

---

## 🛠️ Customization

- **Avatars & Logos:** Replace images in `public/avatars/` and `public/`.
- **Themes:** Edit `public/custom_chainlit.css` for custom styles.
- **Configuration:** Adjust `.chainlit/config.toml` and `.streamlit/config.toml` as needed.

---

## 🤝 Contributing

We welcome contributions! Please open issues or submit pull requests for improvements and new features.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 💡 Credits

Made with ❤️ by the profAi team.

---

> _Empower your team. profAi everything._

## **Overview**
In order to help quickly understand both the visual content and spoken discussion during an event, or an MOOC such as the LLM Agents Berkeley course (which are hours long or multi-day), we want to build an assistant that leverages LLMs to summarize recordings, interpret visuals, and answer follow-up questions related to the event. This system would significantly reduce the time needed to review long events, and would event content more accessible and actionable.

## **Key Features and Functionality**
### **Event Summarization** 
- Summarizes key points from the event, including discussions, keynote presentations, and Q&A sessions.
- The LLM captures the essence of talks and discussions, extracting key themes, recommendations, and conclusions. It can also create topic-based summaries (e.g., by speaker, session, or panel).

### **Visual Content Interpretation (Language + Vision Model)**
- Interprets slides, charts, and any other visual media shared during the event.
- The LLM can relate visual elements (like infographics or data visualizations) to the topics being discussed, providing context and summary explanations.

### **Interactive Q&A System**
- Allows users to ask follow-up questions about specific sessions, speakers, or visual content after the event.
- Answers specific queries like, “What was the main takeaway from Speaker X’s session?” or “What were the key statistics shown in the slide about market trends?”

### **Session Categorization and Indexing**
- Automatically segments and categorizes different parts of the event based on topics, speakers, or themes. Given the longer duration of events, this feature would be critical to ensure smooth navigation of multi-day or multi-session events.
- The LLM organizes event content into searchable categories, making it easy for users to find specific parts of the event they are interested in (e.g., “AI in Healthcare” or “Keynote by John Doe”).

## **Tech Stack**
### Language
- Python >=3.10
- Packages are noted in the requirements.txt

## **How to run the app**
- Make sure you have Python >=3.10 installed
- Setup venv and activate it
    * `python3 -m venv .venv`
    * `source .venv/bin/activate`
- Run `pip install -r requirements.txt` to install the dependencies
- Run `streamlit run Home.py` to start the app
- To enable the Immersive Mode: Run `chainlit run immersive_chainlit.py -w --port 8080` to start the chainlit app before navigating to the immersive mode section in the sidebar.
