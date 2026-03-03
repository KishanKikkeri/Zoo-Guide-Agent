# 🦁 Zoo Guide Agent

Zoo Guide Agent is a cloud-based AI assistant built on Google Cloud Platform (GCP) using Vertex AI.  
It provides intelligent, interactive responses about zoo animals, exhibits, and visitor information while demonstrating secure cloud architecture and IAM best practices.

---

## 🚀 Overview

This project showcases:

- 🤖 AI-powered responses using Vertex AI
- 🔐 Secure authentication via Service Accounts
- 🛡 IAM role management
- ☁️ Cloud-native deployment principles
- 📦 Modular and maintainable project structure

The agent can answer questions about animals, habitats, conservation facts, and general zoo visitor guidance.

---

## 🏗 Architecture

User → Application Layer → Vertex AI → Response  
                          ↑  
                     Service Account (IAM secured)

---

## 🛠 Tech Stack

- Google Cloud Platform (GCP)
- Vertex AI
- IAM & Service Accounts
- gcloud CLI
- Python

---

## ⚙️ Setup Instructions

### 1️⃣ Set Project

```bash
gcloud config set project YOUR_PROJECT_ID
```

### 2️⃣ Create Service Account

```bash
gcloud iam service-accounts create zoo-guide-sa \
    --display-name="Zoo Guide Service Account"
```

### 3️⃣ Grant Vertex AI Access

```bash
gcloud projects add-iam-policy-binding YOUR_PROJECT_ID \
    --member="serviceAccount:zoo-guide-sa@YOUR_PROJECT_ID.iam.gserviceaccount.com" \
    --role="roles/aiplatform.user"
```

### 4️⃣ Authenticate

```bash
gcloud auth application-default login
```

---

## 🔐 Security

- Follows the principle of least privilege
- No hardcoded credentials
- Secure service-to-service authentication
- Uses IAM best practices

---

## 📂 Project Structure

```
zoo_guide_agent/
│
├── main.py
├── requirements.txt
├── config/
├── utils/
└── README.md
```

---

## 💡 Example Queries

- "Tell me about African elephants."
- "What animals are in the reptile exhibit?"
- "When is feeding time for lions?"

---

## 🎯 Learning Objectives

- Configure IAM roles in GCP
- Create and manage service accounts
- Integrate AI APIs securely
- Debug gcloud CLI issues
- Build production-style cloud applications

---

## 🚧 Future Improvements

- Web UI (Streamlit or Flask)
- Deployment to Cloud Run
- Cloud Logging integration
- CI/CD pipeline
- Multi-language support

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss improvements.

---

## 📜 License

This project is for educational and demonstration purposes.