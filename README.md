# jenkins-ci-cd-workflow

What I've done is basically created a custom script that will automate app initialisation, testing and deployment for Jenkins on "Windows Environment" 😵😵😵


---

## ⚙️ Prerequisites

Make sure you have the following set up:

- ✅ Jenkins installed (Windows OS)
- ✅ Jenkins plugins:
  - Git Plugin
  - Pipeline Plugin
- ✅ Git installed and added to `PATH`
- ✅ Node.js and npm installed on the Jenkins host machine

---

## 🧪 What the Pipeline Does

The pipeline defined in `Jenkinsfile` performs the following stages:

### 1. 🧾 Checkout
- Pulls the code from GitHub repository using Jenkins’ SCM.

### 2. 📦 Install Dependencies
- Runs `npm install` to install all required packages.

### 3. 🧪 Test
- Executes `npm test`.
- Currently prints: `"No tests yet"` and exits with success.

### 4. ▶️ Run App
- Starts the Node.js application using:
  ```cmd
  start "" /b cmd /c "npm start"
