# 🦜 LangChain Text Summarizer - YouTube & Website

Ever landed on a 45-minute YouTube video or a massive blog post and thought *"I just need the gist"*? That's exactly why I built this.

Paste a URL - any YouTube video or website - and this app gives you a clean, readable 300-word summary in seconds. No fluff, no scrolling, just the key ideas.

---

## 🚀 What it can do

- **Summarize YouTube videos** - drop in a YouTube link and it pulls the transcript and summarizes it for you
- **Summarize websites & articles** - works on most news articles, blog posts, and web pages
- **Fast as anything** - runs on Groq's inference engine, so you're not sitting around waiting
- **Keeps your API key safe** - entered as a password field, never exposed in the UI

---

## 🛠️ Built with

| Tool | What it does here |
|---|---|
| [Streamlit](https://streamlit.io/) | The whole UI, dead simple to use |
| [LangChain](https://www.langchain.com/) | Handles the summarization logic and LLM chaining |
| [Groq API](https://groq.com/) | Powers the fast inference |
| [Gemma-7b-It](https://huggingface.co/google/gemma-7b-it) | The actual model doing the summarizing |
| [YoutubeLoader](https://python.langchain.com/docs/integrations/document_loaders/youtube_transcript) | Grabs YouTube transcripts |
| [UnstructuredURLLoader](https://python.langchain.com/docs/integrations/document_loaders/url) | Scrapes and loads web page content |

---

## ⚙️ Getting it running locally

It's pretty straightforward. You'll need Python 3.8+ and a free Groq API key (takes about 2 minutes to get one).

**1. Clone the repo**

```bash
git clone https://github.com/your-username/text-summarization.git
cd text-summarization
```

**2. Set up a virtual environment** *(optional but recommended)*

```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
```

**3. Install the dependencies**

```bash
pip install -r requirements.txt
```

**4. Run it**

```bash
streamlit run app.py
```

Then head to `http://localhost:8501` in your browser and you're good to go.

---

## 🔑 Getting a Groq API Key

1. Go to [console.groq.com](https://console.groq.com)
2. Sign up for a free account
3. Hit **API Keys** and create a new key
4. Copy it and paste it into the app's sidebar when you run it

---

## 🖥️ How to use it

1. Open the app and paste your **Groq API Key** into the sidebar
2. Drop a **URL** into the input box - YouTube link or any website
3. Click **"Summarize the Content from YT or Website"**
4. Give it a few seconds and your summary will appear below

That's it. No complicated setup, no config files.

---

## 📁 What's in this repo

```
text-summarization/
│
├── app.py                        # The Streamlit app - this is the main thing
├── requirements.txt              # Everything you need to install
├── text_summarization.ipynb      # Jupyter notebook
├── apjspeech.pdf                 # Sample document used for testing
└── README.md                     # You're reading it
```

---

## 🙋 A few things worth knowing

- YouTube summarization only works if the video has **captions or a transcript**. If it doesn't, it'll throw an error
- Some websites actively block scrapers, so it won't work on every page
- SSL verification is turned off for URL loading, so stick to sites you trust

---

## 🙌 Shoutout to

- [LangChain](https://www.langchain.com/) - made chaining all this together surprisingly painless
- [Groq](https://groq.com/) - the inference speed is genuinely impressive
- [Streamlit](https://streamlit.io/) - for making Python web apps feel easy

---

## 📄 License

MIT - do whatever you want with it.
