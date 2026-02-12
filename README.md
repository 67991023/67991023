<div align="center">

# 🛡️ 67991023

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,3,5,6&height=200&section=header&text=Security%20%7C%20Backend%20%7C%20AI&fontSize=45&fontColor=fff&animation=fadeIn&fontAlignY=35&desc=Breaking%20Systems%20×%20Building%20Solutions%20×%20Machine%20Learning&descAlignY=55&descSize=16" width="100%"/>

### 🔐 **Cybersecurity Researcher | Full-Stack Engineer | AI/ML Developer**

```python
class Developer:
    def __init__(self):
        self.name = "67991023"
        self.role = "Security Researcher & Full-Stack Engineer"
        self.location = "🇹🇭 Thailand"
        self.interests = [
            "Web Security & Penetration Testing",
            "Backend Architecture & DevOps",
            "Machine Learning & NLP",
            "Log Management & Observability"
        ]
        self.mindset = "Security by design, Scalability by default"
        self.status = "🔥 Building secure, scalable systems"
    
    def get_tech_stack(self):
        return {
            "security": ["Golang", "Nuclei", "Burp Suite", "OAST"],
            "backend": ["Python", "FastAPI", "Node.js", "WebSocket"],
            "ai_ml": ["scikit-learn", "K-Means", "NLP", "Thai Text Processing"],
            "devops": ["Docker", "OpenSearch", "Vector", "Nginx"],
            "frontend": ["React", "Vite", "Chart.js", "TailwindCSS"]
        }
```

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=3000&pause=1000&color=F75C7E&center=true&vCenter=true&multiline=false&repeat=true&width=800&lines=Golang+%7C+Python+%7C+Node.js+%7C+Security+Tools;Web+Scanner+%7C+Log+Management+%7C+ML+Classification;Docker+%7C+Microservices+%7C+Real-time+Systems;From+vulnerability+discovery+to+production+deployment+⚡" alt="Typing SVG" />
</p>

[![GitHub followers](https://img.shields.io/github/followers/67991023?style=social)](https://github.com/67991023)
[![GitHub Stars](https://img.shields.io/github/stars/67991023?style=social)](https://github.com/67991023)

</div>

---

## 🎯 **About Me**

ผมเป็น **Security Researcher** และ **Full-Stack Developer** ที่หลงใหลในการ **สร้างเครื่องมือ Security Tools**, **ออกแบบระบบ Backend ขนาดใหญ่**, และ **พัฒนา AI/ML Applications** สำหรับการวิเคราะห์ข้อมูล

💡 **Philosophy:**  
> "การรักษาความปลอดภัยที่ดีที่สุด คือการเข้าใจมุมมองของ Attacker และสร้างระบบที่ทน Robust ตั้งแต่ต้น"

🔍 **What I Do:**
- 🛡️ พัฒนา **Web Vulnerability Scanners** และเครื่องมือ **Penetration Testing**
- ⚙️ สร้าง **Full-Stack Log Management Systems** แบบ Enterprise-grade
- 🤖 ออกแบบ **AI/ML Systems** สำหรับ Thai Language Processing และ Text Classification
- 🏗️ พัฒนา **Microservices Architecture** ด้วย Docker และ API Gateway
- 📊 สร้าง **Real-time Dashboards** สำหรับ Monitoring และ Visualization

---

## 🚀 **Featured Projects**

### 🔥 [BurpSuitePro_Fake](https://github.com/67991023/BurpSuitePro_Fake) - **Web Vulnerability Scanner**
> **Educational Security Tool** เขียนด้วย **Golang** เพื่อเรียนรู้การทำงานของ Burp Suite Pro

**🎯 Key Features:**
- **Intercept Proxy** - ดักจับและแก้ไข HTTP/HTTPS Traffic
- **Auto Discovery** - Crawler + Fuzzer สำหรับค้นหา Hidden Endpoints
- **Vulnerability Scanner** - SQL Injection & XSS Detection
- **Repeater** - Manual Request Modification Tool
- **Real-time Dashboard** - WebSocket-based Live Monitoring
- **OAST Integration** - Out-of-Band Interaction Detection
- **Nuclei Bridge** - Integration with Nuclei Templates

**💻 Tech Stack:**  
`Golang` `TLS/Certificate Handling` `HTTP Proxy` `Goroutines` `WebSocket` `Nuclei` `OAST`

```go
// Example: Proxy Architecture
func main() {
    targetDomain = "example.com"
    oastService, _ := StartOAST()
    caCert, _ := tls.LoadX509KeyPair("ca.crt", "ca.key")
    
    go startDashboardServer()  // WebSocket Dashboard
    go StartCrawler(target)    // Auto Discovery
    go RunNucleiScan(host)     // Vulnerability Scanning
    
    proxyServer := &http.Server{
        Addr: ":8080",
        Handler: http.HandlerFunc(handleProxy),
    }
}
```

**🔗 Links:**
- 📖 [Full Documentation](https://github.com/67991023/BurpSuitePro_Fake)
- 📊 เปรียบเทียบ PortSwigger vs OpenBurp Pro (Excel file included)

---

### 📊 [CompleteLogManagement](https://github.com/67991023/CompleteLogManagement) - **Enterprise Log Management System**
> **Full-Stack Log Management Platform** สำหรับ Ingestion, Storage, Search, Visualization, และ Alerting

**🎯 Key Features:**
- **Multi-Source Ingestion** - Syslog (UDP/TCP), HTTP JSON, File Batch
- **Centralized Storage** - OpenSearch with Optimized Indexing
- **Real-time Search** - Fast Full-text Search with Filters
- **Interactive Dashboard** - React + Vite with Charts (Chart.js)
- **Alerting System** - Configurable Rules with Webhook Notifications
- **Authentication & Authorization** - JWT-based with RBAC (Admin/Viewer)
- **Multi-Tenant Support** - Data Isolation per Tenant
- **Data Retention** - Automatic Cleanup after 7 Days
- **Two Deployment Modes** - Appliance (Docker Compose) + SaaS (Cloud HTTPS)

**💻 Tech Stack:**  
`Python/FastAPI` `React` `Vite` `OpenSearch` `Vector` `Docker Compose` `JWT` `APScheduler` `TailwindCSS` `Nginx`

```python
# Backend: FastAPI with JWT Authentication
from fastapi import FastAPI, Depends, HTTPException
from jose import JWTError, jwt

app = FastAPI()

@app.post("/api/login")
async def login(credentials: LoginRequest):
    user = authenticate_user(credentials.username, credentials.password)
    if not user:
        raise HTTPException(status_code=401, detail="Invalid credentials")
    token = create_jwt_token(user)
    return {"token": token, "role": user.role, "tenant": user.tenant}

@app.get("/api/search")
async def search_logs(q: str, current_user: User = Depends(get_current_user)):
    results = opensearch_client.search(
        index=f"logs-{current_user.tenant}-*",
        body={"query": {"query_string": {"query": q}}}
    )
    return results
```

**Architecture:**
```
Log Sources → Vector (Collector) → OpenSearch (Storage) 
    → FastAPI (Backend) → React (Dashboard)
```

**🔗 Links:**
- 📖 [Full Documentation](https://github.com/67991023/CompleteLogManagement)
- 🎬 [Architecture Diagram](https://github.com/67991023/CompleteLogManagement#architecture)

---

### 🤖 [recorderAI](https://github.com/67991023/recorderAI) - **Thai Voice Recorder with ML Analytics**
> **AI-powered Voice Recognition System** สำหรับ Thai Language พร้อม Machine Learning Classification

**🎯 Key Features:**
- **Thai Speech Recognition** - Google Speech-to-Text API
- **ML Text Classification** - K-Means Clustering with TF-IDF
- **Thai Text Processing** - Custom Word Count & Validation
- **Data Visualization** - Matplotlib Charts & Comprehensive Dashboard
- **Analysis Reports** - Automated PDF/Text Report Generation
- **RESTful API** - FastAPI for Web Integration
- **Docker Support** - Containerized Deployment
- **Frontend Dashboard** - React-based UI for Recording Management

**💻 Tech Stack:**  
`Python` `scikit-learn` `K-Means` `TF-IDF` `SpeechRecognition` `pythainlp` `Matplotlib` `FastAPI` `Docker` `PostgreSQL`

```python
# ML Classification Pipeline
def ml_text_classification(voice_records):
    texts = [record['text'] for record in voice_records]
    
    # TF-IDF Vectorization
    vectorizer = TfidfVectorizer(max_features=50)
    X = vectorizer.fit_transform(texts)
    
    # K-Means Clustering
    n_clusters = min(3, len(texts))
    kmeans = KMeans(n_clusters=n_clusters, random_state=42)
    clusters = kmeans.fit_predict(X)
    
    # Create DataFrame with Results
    results_df = pd.DataFrame({
        'text': texts,
        'cluster': clusters,
        'word_count': [fix_thai_word_count(t) for t in texts]
    })
    
    return results_df, vectorizer, kmeans
```

**🔗 Links:**
- 📖 [Architecture Documentation](https://github.com/67991023/recorderAI/blob/master/ARCHITECTURE.md)
- 🎬 [Deployment Guide](https://github.com/67991023/recorderAI/blob/master/DEPLOYMENT.md)

---

### 💊 [MoodTrack](https://github.com/67991023/MoodTrack) - **Mental Health Tracking Application**
> **Full-Stack Mood Tracking Platform** สำหรับ Monitor อารมณ์และสุขภาพจิตประจำวัน

**🎯 Key Features:**
- **Mood Logging** - บันทึกอารมณ์พร้อม Emoji Selector
- **Mood Analytics** - กราฟวิเคราะห์อารมณ์ในแต่ละวัน/สัปดาห์/เดือน
- **Journal Entry** - เขียน Journal พร้อม Rich Text Editor
- **Authentication** - JWT-based Login System
- **Data Visualization** - Chart.js for Mood Trends
- **Responsive Design** - Mobile-first Approach
- **Deployment Ready** - Vercel-optimized

**💻 Tech Stack:**  
`Node.js` `Express` `MongoDB` `EJS Templates` `Chart.js` `JWT` `Vercel`

---

### 🛡️ [aegis_backend](https://github.com/67991023/aegis_backend) - **Microservices Architecture Backend**
> **Spring Boot Microservices** with Service Discovery, API Gateway, และ AI Service Integration

**🎯 Key Features:**
- **API Gateway** - Centralized Entry Point
- **Service Discovery** - Eureka Server
- **Authentication Service** - Spring Security + JWT
- **AI Service** - ML Model Integration
- **Microservices Pattern** - Independent Services

**💻 Tech Stack:**  
`Java` `Spring Boot` `Spring Cloud` `Eureka` `Spring Security` `Microservices Architecture`

---

## 💻 **Tech Stack & Skills**

### 🔐 **Security & Penetration Testing**
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp%20Suite-FF6633?style=for-the-badge&logo=burp-suite&logoColor=white)
![Nuclei](https://img.shields.io/badge/Nuclei-000000?style=for-the-badge&logo=nuclei&logoColor=white)
![OAST](https://img.shields.io/badge/OAST-FF4500?style=for-the-badge&logo=security&logoColor=white)

**Expertise:**
- Web Vulnerability Scanning (SQL Injection, XSS, SSRF)
- Proxy & Traffic Interception
- Out-of-Band Interaction Detection
- CTF Problem Solving

### ⚙️ **Backend & API Development**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)

**Expertise:**
- RESTful API Design
- WebSocket Real-time Communication
- JWT Authentication & RBAC
- Microservices Architecture

### 🤖 **AI & Machine Learning**
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-4285F4?style=for-the-badge&logo=google&logoColor=white)

**Expertise:**
- K-Means Clustering
- TF-IDF Vectorization
- Thai Language Processing
- Text Classification

### 🗄️ **Databases & Storage**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![OpenSearch](https://img.shields.io/badge/OpenSearch-005EB8?style=for-the-badge&logo=opensearch&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

### 🎨 **Frontend & Visualization**
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

### 🛠️ **DevOps & Tools**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

---

## 📊 **GitHub Stats**

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=67991023&show_icons=true&theme=radical&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=F75C7E&icon_color=F75C7E&text_color=C9D1D9"/>
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=67991023&layout=compact&langs_count=8&theme=radical&hide_border=true&bg_color=0D1117&title_color=F75C7E&text_color=C9D1D9"/>

</div>

<div align="center">

[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=67991023&theme=radical&hide_border=true&background=0D1117&stroke=F75C7E&ring=F75C7E&fire=FF6B6B&currStreakLabel=F75C7E)](https://git.io/streak-stats)

</div>

---

## 🏆 **Highlight Skills**

<div align="center">

```mermaid
mindmap
  root((67991023))
    Security
      Web Vulnerability Scanning
      Penetration Testing
      OAST Detection
      CTF Challenges
    Backend
      API Development
      Microservices
      Real-time Systems
      Authentication & Authorization
    AI/ML
      Text Classification
      NLP Thai Language
      K-Means Clustering
      Data Visualization
    DevOps
      Docker Containerization
      Log Management
      CI/CD Pipeline
      Cloud Deployment
```

</div>

---

## 🎯 **Current Focus**

🔭 **Working On:**
- 🛡️ Enhancing **BurpSuitePro_Fake** with Advanced Scanning Techniques
- 📊 Scaling **CompleteLogManagement** for High-Volume Logs (>10K logs/sec)
- 🤖 Improving **recorderAI** ML Models for Better Thai Text Classification

🌱 **Learning:**
- 🔐 Advanced Web Application Firewall (WAF) Bypass Techniques
- ☁️ Kubernetes & Cloud-Native Security
- 🧠 Deep Learning for Security Anomaly Detection

💬 **Ask Me About:**
- Web Security & Vulnerability Assessment
- Building Scalable Backend Systems
- Machine Learning for Text Analysis
- Full-Stack Development Best Practices

---

## 📫 **Connect With Me**

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/67991023)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@example.com)

</div>

---

## 📄 **License**

Most of my projects are licensed under the **MIT License** - see individual project repositories for details.

---

<div align="center">

### 💡 *"Security is not a product, but a process. Build it right from the start."*

**⚡ Let's build secure, scalable, and intelligent systems together! ⚡**

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,3,5,6&height=120&section=footer" width="100%"/>

</div>
