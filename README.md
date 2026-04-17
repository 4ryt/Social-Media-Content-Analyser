# 📊 Social Media Content Analyzer

A machine learning–powered web application that analyzes user interactions across multiple social media platforms and generates sentiment-based insights in real time.

---

## 🚀 Overview

This application collects posts and comments from Instagram, Threads, and X (Twitter), and applies a transformer-based sentiment analysis model to classify user responses as **Positive, Neutral, or Negative**.

It provides:

* A **unified dashboard** for combined insights
* **Platform-specific analysis pages**
* **Interactive visualizations** with filtering options

---

## 🧠 Key Features

* 🔗 Multi-platform integration (Instagram, Threads, X)
* 💬 Real-time extraction of comments and replies
* 🧠 Sentiment analysis using RoBERTa model
* 📊 Pie chart visualization of sentiment distribution
* 🎯 Filter insights by sentiment (Positive / Neutral / Negative)
* 📅 Analyze data by post or date
* ⚡ Async API calls with loading indicators
* 🔐 Secure API key handling via environment variables

---

## 🏗️ Architecture

### Backend (Flask)

* Handles API requests and routing
* Fetches data from social media APIs
* Performs sentiment analysis


---

### Frontend

#### Dashboard Page

* Select multiple platforms
* View combined insights
* Sentiment distribution chart


#### Platform-Specific Page

* Analyze individual platform data
* Filter by caption/thread/date/status ID
* Dynamic chart + sentiment filtering


---

## 🛠️ Tech Stack

* **Backend:** Flask
* **Frontend:** HTML, CSS, Bootstrap, JavaScript
* **ML Model:**

  * `cardiffnlp/twitter-roberta-base-sentiment`
* **APIs:**

  * Instagram Graph API
  * Threads API
  * X (Twitter) API
* **Visualization:** Chart.js

---

## ⚙️ Installation

```bash
git clone https://github.com/your-username/social-media-content-analyzer.git
cd social-media-content-analyzer
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file in the root directory:

```env
X_BEARER_TOKEN=your_x_token
INSTAGRAM_ACCESS_TOKEN=your_instagram_token
THREADS_ACCESS_TOKEN=your_threads_token
INSTAGRAM_USER_ID=your_instagram_user_id
X_USER_ID=your_x_user_id
```

---

## ▶️ Run the Application

```bash
python app.py
```

Open in browser:

```
http://localhost:5000
```

---

## 📊 How It Works

1. User selects platforms or specific posts
2. Backend fetches data via APIs
3. Text is processed through RoBERTa model
4. Sentiment is classified
5. Results are visualized with charts and filters

---

## 📌 API Endpoint

### `POST /api/insights`

**Request Body Examples:**

```json
{
  "platforms": ["Instagram", "Threads"]
}
```

```json
{
  "platform": "Instagram",
  "caption": "POST_ID"
}
```

```json
{
  "platform": "X",
  "status_id": "TWEET_ID"
}
```

---

## ⚠️ Limitations

* X (Twitter) API has rate limits (cooldown applies)
* Requires valid API credentials
* Depends on external API availability

---

## 🔮 Future Improvements

* Add support for LinkedIn & YouTube
* Advanced NLP (emotion detection, topic modeling)
* User authentication & saved dashboards
* Deployment (Docker + Cloud)

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first.

---

