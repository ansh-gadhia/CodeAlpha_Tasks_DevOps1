# 🚀 Azure CI/CD Flask App Deployment

This project demonstrates the implementation of a **CI/CD (Continuous Integration and Continuous Deployment) pipeline** using **Azure DevOps** to deploy a **Flask web application** to **Azure App Service**.
Here is the YAML File that I used for setting up the Pipelines.
> ✅ Created as part of my **DevOps Internship at CodeAlpha**.

---

## 🔧 Technologies Used

- **Azure DevOps Pipelines**
- **Azure App Service (Linux)**
- **Self-hosted Agent**
- **Flask (Python Web Framework)**
- **GitHub & Azure Repos**

---

## 📁 Repository Structure

```
project/
├── hello_app/
│   ├── __init__.py       # Flask app instance
│   ├── views.py          # Application routes
│   ├── webapp.py         # Entry point for the app
├── templates/            # HTML templates
├── static/               # Static files (CSS, JS, JSON)
├── requirements.txt      # Dependencies (Flask, gunicorn)
├── azure-pipelines.yml   # CI/CD pipeline definition
```

---

## ⚙️ CI/CD Pipeline (azure-pipelines.yml)

This file defines the entire CI/CD process:

- Uses a **self-hosted agent**
- Installs Python & project dependencies
- Archives the app into a ZIP
- Deploys to **Azure Web App** using the `AzureWebApp@1` task

---

## 🌐 Live Deployment Setup

1. **Create an Azure App Service (Linux)**  
2. Set the following **Application Settings** in the App Service:

| Name              | Value                                 |
|-------------------|----------------------------------------|
| `WEBSITES_PORT`   | `5000`                                 |
| `STARTUP_COMMAND` | `gunicorn hello_app.webapp:app`        |

3. **Connect Azure DevOps pipeline** to Azure App Service via a **Service Connection**
4. Every commit to the main branch triggers the pipeline and deploys the latest version

---

## 💻 Flask App Code

🔗 **Source Code:**  
[➡️ GitHub - Flask App Repo](https://github.com/ansh-gadhia/SimpleFlaskWebApp)

---

## 🎬 Demo Video

Check out the full demo on LinkedIn:  
[📺 Watch the CI/CD demo](https://www.linkedin.com/in/ansh-gadhia)

---

## 🤝 Acknowledgements

This project was completed under the **DevOps Internship Program** at **CodeAlpha**.  
Thanks to the mentors and team for their guidance and support!
