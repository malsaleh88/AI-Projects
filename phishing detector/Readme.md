# 🛡️ Phishing Detector - n8n Workflow

## 📌 Introduction to n8n

[n8n](https://n8n.io/) is an **open-source workflow automation tool** that allows you to **connect different applications and automate processes**. It provides a **low-code environment** where you can build complex workflows visually.

With **n8n**, you can:
- Automate data transfers between apps.
- Integrate APIs and services.
- Process and analyze data with **AI-powered tools**.


## 🚀 How to Start with n8n

### 🛠 **Installation & Setup**
1. **Install n8n**:
   ```bash
   npm install -g n8n
![99](https://github.com/user-attachments/assets/2afe8878-2064-4550-8a6e-076d944ef85e)


---



## 🔍 About the AI-Powered Phishing Detector

This workflow is designed to **automatically detect phishing emails** by analyzing email content using **Google Gemini AI**. It follows a structured approach to analyze email headers and body text.

### ✨ **What This Workflow Does**
1. **Fetches emails** from a **Gmail inbox** using Google Cloud API.
![1](https://github.com/user-attachments/assets/5c4e354c-b282-430c-bbc4-3fe0b56a6d99)


2. **Extracts important details** (Sender, Subject, Email Snippet).

![2](https://github.com/user-attachments/assets/8ef80d25-0659-4414-8a9b-a16cffd7038e)
![3](https://github.com/user-attachments/assets/c95d2ed6-5e47-47ed-b702-596f019b2772)

3. **Analyzes the email content** using **Google Gemini AI**.
![4](https://github.com/user-attachments/assets/ed9a2969-62ac-42c1-84d0-a4484e4b0960)

4. **Classifies the email** as **Phishing** or **Safe Email**.
![5](https://github.com/user-attachments/assets/55a399ab-5f72-486f-a766-7ae0f2deeda1)

---




## 🔄 How This Workflow Works

### 1️⃣ Retrieve Emails from Gmail
- Uses **Gmail API** via **Google Cloud OAuth 2.0 credentials**.
- Fetches recent **unread emails** for analysis.

### 2️⃣ Extract & Filter Email Details
- Uses **Edit Fields (Set Node)** to extract:
  - 📧 **Sender** (From field)
  - 📝 **Subject** (Subject field)
  - 📄 **Email Body (Snippet)** (`snippet` field)

### 3️⃣ Analyze the Email with Google Gemini AI
- Sends extracted data to **Google Gemini AI**.
- Uses a **predefined prompt** to analyze the email for phishing.

### 4️⃣ AI Decision Making

If phishing is detected, the workflow returns:
```plaintext
Phishing Detected
