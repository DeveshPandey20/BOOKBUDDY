
# 📚 BOOKBUDDY

An intelligent book recommendation chatbot built using **IBM Watson Assistant**, optionally supported by a backend service for enhanced functionality.

---

## 🧠 Overview

**BOOKBUDDY** offers users interactive book suggestions through a conversational interface. It leverages Watson Assistant for natural language understanding and can fetch book data using APIs or curated lists.

---

## 🚀 Key Features

- Suggests books based on genre, topic, or author preferences  
- Can integrate with external APIs for dynamic recommendations  
- Simple conversation flow with instantly useful responses  
- Lightweight and easy to deploy on static or dynamic websites  

---

## 🛠️ Getting Started

### Prerequisites

- A published IBM Watson Assistant Dialog Skill  
- Integration credentials: `integrationID`, `region`, and `serviceInstanceID` from Watson Assistant Web Chat settings

### Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/DeveshPandey20/BOOKBUDDY.git
   cd BOOKBUDDY
   ```

2. (Optional) If a backend service is used:
   - Install dependencies:
     ```bash
     npm install   # or pip install -r requirements.txt
     ```

3. Add your Watson Assistant credentials to an `.env` file (or embed directly):
   ```
   WATSON_INTEGRATION_ID=your_integration_id
   WATSON_REGION=your_region  # e.g. us-south
   WATSON_SERVICE_INSTANCE_ID=your_service_instance_id
   ```

4. If there's a backend service, start it:
   ```bash
   npm start     # or python app.py
   ```

---

## Embed the Chatbot on Your Website

Add the following snippet into your **`index.html`**, just before the closing `</body>` tag:

```html
<script>
  window.watsonAssistantChatOptions = {
    integrationID: "YOUR_INTEGRATION_ID",
    region: "YOUR_REGION",
    serviceInstanceID: "YOUR_SERVICE_INSTANCE_ID",
    onLoad: function(instance) {
      instance.render();
    }
  };
  setTimeout(function() {
    const s = document.createElement('script');
    s.src = "https://web-chat.global.assistant.watson.appdomain.cloud/versions/latest/WatsonAssistantChatEntry.js";
    document.head.appendChild(s);
  });
</script>
```

---

## 📂 Project Structure (if applicable)

```
BOOKBUDDY/
├── public/
│   └── index.html       ← Embed snippet here
├── src/                 ← optional backend code
│   ├── server.js
│   └── bookData.json
├── .env
└── README.md
```

---

## 🧩 How It Works

1. User interacts with the chatbot UI on your site.  
2. Watson Assistant processes user input.  
3. If a backend exists, it retrieves book suggestions (e.g. via APIs).  
4. Assistant responds with recommended books in conversational format.

---

## 🙌 Example Dialogue

- **User**: “Suggest a thriller book.”  
- **Bot**: “You might enjoy *Gone Girl* by Gillian Flynn. Need another?”  
- **User**: “Yes.”  
- **Bot**: “Try *The Girl on the Train*—very gripping!”

---

## 🤝 Contributing

Contributions welcome! You can help by:

- Adding support for APIs (e.g. Google Books)
- Improving dialogue or expanding book data
- Enhancing UI or supporting multiple languages

Steps:
```bash
git fork https://github.com/DeveshPandey20/BOOKBUDDY.git
git checkout -b your-feature-branch
# Add your changes → commit → push → create pull request
```

---

## 📄 License

This project is under the **MIT License** — see the `LICENSE` file for details.

---

## ✅ Resources

- [Watson Assistant Documentation](https://cloud.ibm.com/docs/assistant)  
- [Google Books API](https://developers.google.com/books)  
