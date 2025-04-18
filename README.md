# ⚙️ Task 8: Run a Simple Java Maven Build Job in Jenkins

## 📌 Internship Task Overview

This task demonstrates the basics of **CI/CD using Jenkins and Maven**. The goal is to build a simple Java application using Jenkins Freestyle job and Maven build system.

---

## 🎯 Objective

> Set up Jenkins and configure a Maven-based Freestyle job to build a basic Java project. Learn how Jenkins executes a build pipeline using Maven.

---

## 🛠 Tools & Technologies Used

| Tool       | Purpose                              |
|------------|--------------------------------------|
| Jenkins    | Continuous Integration server        |
| Java JDK   | To compile the Java application      |
| Maven      | To automate the build process        |
| Git        | (Optional) Source code versioning    |
| Docker     | (Optional) Containerized Jenkins     |
| Browser    | To access Jenkins UI                 |

---

## 📁 Project Structure

# ⚙️ Task 8: Run a Simple Java Maven Build Job in Jenkins

## 📌 Internship Task Overview

This task demonstrates the basics of **CI/CD using Jenkins and Maven**. The goal is to build a simple Java application using Jenkins Freestyle job and Maven build system.

---

## 🎯 Objective

> Set up Jenkins and configure a Maven-based Freestyle job to build a basic Java project. Learn how Jenkins executes a build pipeline using Maven.

---

## 🛠 Tools & Technologies Used

| Tool       | Purpose                              |
|------------|--------------------------------------|
| Jenkins    | Continuous Integration server        |
| Java JDK   | To compile the Java application      |
| Maven      | To automate the build process        |
| Git        | (Optional) Source code versioning    |
| Docker     | (Optional) Containerized Jenkins     |
| Browser    | To access Jenkins UI                 |

---

## 📁 Project Structure

![Screenshot 2025-04-19 002714](https://github.com/user-attachments/assets/e809e74a-0c0a-494e-a254-78d6d4b0426c)

### 🚀 Step-by-Step Instructions
### 🔹 1. Start Jenkins (via Docker)
```bash

docker run -p 8080:8080 jenkins/jenkins:lts
```
Access Jenkins UI at:
```
👉 http://localhost:8080
```
### 🔹 2. Unlock Jenkins
Get the password from container logs:

```bash

docker exec -it <container_id> cat /var/jenkins_home/secrets/initialAdminPassword
```
### 🔹 3. Configure Maven in Jenkins
Go to: Manage Jenkins → Global Tool Configuration

Under Maven:
```
Add Maven 3.8.6
```
✅ Check "Install automatically"

Under JDK: Ensure Java 8 or 11 is configured

### 🔹 4. Create the Jenkins Job
Click New Item → Freestyle Project
```
Name it: Build-Java-App

Under Source Code Management:

Git: https://github.com/Raj9536/internship-task-8.git

Under Build:

Invoke top-level Maven targets

Maven Version: Maven 3.8.6

Goals: clean package
```
### 🔹 5. Build and Verify
Click Build Now

Go to Console Output

✅ Look for: BUILD SUCCESS

📸 Screenshot
![Screenshot 2025-04-19 002633](https://github.com/user-attachments/assets/fdadef64-78e1-42e9-83d1-4e9992a2c77a)
![Screenshot 2025-04-19 002618](https://github.com/user-attachments/assets/6cd75af1-1545-41a8-b5e4-f3e513f9b43f)


### 📘 Key Learnings
How to use Jenkins Freestyle jobs

How to trigger manual builds

How Maven compiles and packages Java projects

Jenkins tool configuration and console output analysis
