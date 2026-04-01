# 🚀 Simple Java Web App (Docker + Tomcat + Maven)

This is a minimal Java web application built using **Servlet + JSP**, packaged as a **WAR file**, and deployed using **Apache Tomcat inside Docker**.

This project is designed for learning and practicing:

* Maven build lifecycle
* WAR packaging
* Docker image creation
* Container deployment
* Basic DevOps workflow

---

## 🧱 Tech Stack

* Java 17
* Maven
* Apache Tomcat 10
* Docker

---

## 📁 Project Structure

```
simple-app/
├── pom.xml
├── Dockerfile
└── src/
    └── main/
        ├── java/
        │   └── com/example/HelloServlet.java
        └── webapp/
            ├── index.jsp
            └── WEB-INF/
                └── web.xml
```

---

## ⚙️ Build the Application

Make sure Maven is installed (or use Docker build stage).

```bash
mvn clean package
```

This will generate:

```
target/simple-app.war
```

---

## 🐳 Build Docker Image

```bash
docker build -t simple-app .
```

---

## 🚀 Run the Application

```bash
docker run -d -p 8080:8080 --name simple-app simple-app
```

---

## 🌐 Access the App

Open in browser:

```
http://localhost:8080
```

Click on:

```
/hello
```

---

## 📦 Docker Hub Usage

If image is pushed to Docker Hub:

```bash
docker pull tsrvanam/simple-app:latest
docker run -d -p 8080:8080 tsrvanam/simple-app:latest
```

---

## 🧠 How It Works

1. Maven builds the `.war` file
2. Docker image is created using Tomcat base image
3. WAR is copied into `/usr/local/tomcat/webapps/ROOT.war`
4. Tomcat automatically deploys the application
5. Container exposes port `8080`

---

## 🔥 DevOps Flow

```
Code → Maven Build → Docker Image → Push to Docker Hub → Run Container
```

---


## 👤 Author

**Sravanam Thirupathi Rao**

---

## ⭐ If you found this helpful

Give this repo a ⭐ and keep learning DevOps 🚀
