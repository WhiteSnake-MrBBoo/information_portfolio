<div align="center">
  <h1>JAVA · PYTHON · FLASK · Backend · AI_VISION · CV Engineer · LLM </h1>

  <!-- Tech stack badges -->
  <p align="center">
    <a href="https://www.java.com/"><img src="https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white" /></a>
    <a href="https://spring.io/projects/spring-boot"><img src="https://img.shields.io/badge/Spring%20Boot-3.4-6DB33F?logo=springboot&logoColor=white" /></a>
    <a href="https://modelmapper.org/"><img src="https://img.shields.io/badge/ModelMapper-DI-FF6F00" /></a>    
    <a href="https://www.thymeleaf.org/"><img src="https://img.shields.io/badge/Thymeleaf-View-005F0F?logo=thymeleaf&logoColor=white" /></a>
    <a href="https://adoptium.net/temurin/releases/?version=21"><img src="https://img.shields.io/badge/JDK-21-007396?logo=java&logoColor=white" /></a>
    <a href="https://mariadb.org/"><img src="https://img.shields.io/badge/MariaDB-Server-003545?logo=mariadb&logoColor=white" /></a>   
    <a href="https://github.com/ultralytics/ultralytics"><img src="https://img.shields.io/badge/YOLO-v11-222222" /></a>
    <a href="https://www.kernel.org/"><img src="https://img.shields.io/badge/Linux-Server-FCC624?logo=linux&logoColor=black" /></a>
    <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white" /></a>
    <a href="https://flask.palletsprojects.com/"><img src="https://img.shields.io/badge/Flask-Framework-000000?logo=flask&logoColor=white" /></a>
    <a href="https://opencv.org/"><img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?logo=opencv&logoColor=white" /></a><br>
    <a href="https://www.uipath.com/"><img src="https://img.shields.io/badge/UiPath-VB.NET%20Invoke%20Code-FA4616?logo=uipath&logoColor=white" /></a>
    <a href="https://aws.amazon.com/"><img src="https://img.shields.io/badge/AWS-Cloud-232F3E?logo=amazon-aws&logoColor=white" /></a>
  </p>

  <p>
    <a href="README.md">한국어</a> ·
    <a href="mailto:mrbulsapabb@gmail.com">Email</a>  
    <!-- <a href="https://www.linkedin.com/in/your-id">LinkedIn</a> -->
  </p>
</div>

---

## 👋 Team Projects
- Built the **HexaStay ERP ecosystem (Hotel Admin)** with Spring Boot 3.4 + Thymeleaf + **WebSocket (bi-directional)** + MariaDB.
- Guest-facing **QR authentication & email notifications** + **AI-driven interface** (end-user UI/UX).
- **SPRING BOOT: ModelMapper · Principal** for reliable backend CRUD and an advanced **Admin Dashboard (UI/UX)**.
- **YOLO + OpenCV** CCTV Vision AI dashboard (region alerts, real-time charts, responsive UI).
- **UiPath RPA** pipeline for large-scale text summarization/structuring (Invoke Code, JSON parsing, Excel automation).

---

## 🏆 Featured Projects
> One-click access to **Problem → Approach → Impact → Tech Stack**.  
> > **Click the image** to open the detailed case study document.

### 1) HexaStay Admin – Hotel Management Dashboard
**Stack:** Spring Boot 3.4, JDK 21, Thymeleaf, Bootstrap 5, MariaDB, ModelMapper, AWS, **WebSocket (bi-directional)**  
**Key Features:**  
- Room/Member/Reservation modules with **QR authentication** & **Email notifications**  
  (auto-composed body on reservation: member name / check-in/out / room code / QR link)  
- Status-based room lists (check-in / check-out / show / hide) with **shared `roomlist.html`**  
- **Modal-based** search/edit (HotelRoom image/meta), @Query + Service(ModelMapper) + JSON responses  

**Impact (examples):**  
- Reduced manual operations; **shorter steps** for create/update/notify flows  
- **Convenience for guests** via QR flow  
- AI inference aids **guest decision-making**  
- **Real-time alerts** between guest and admin using WebSocket  
- **Front-end maintainability** via single-page reuse  
> **Click the image to open the Git detailed page**

<!-- Card 1 -->
<div align="center">
  <a href="docs/hexastay-admin.md">
    <img src="assets/hexastay-admin-overview.png" alt="HexaStay Admin" width="820">
  </a>
</div>

---

### 2) CCTV Vision AI Dashboard
**Stack:** Python, Ultralytics YOLOv11, OpenCV, JS/Canvas (Polygon), Threading (real-time/async), Flask/Socket.IO  
**Key Features:**  
- Polygon **Region**-based intrusion counting, real-time alerts (ALERT / WARN / SAFE / IDLE)  
- Responsive UI + **real-time charts/graphs** + **unlimited alert panels**  
- Coordinate normalization, modular YOLO result processing (test/extension friendly)

**Impact (examples):**  
- Single-screen **situational awareness** and **faster decision-making**  
- Region-level alerts enable **false/miss detection feedback loops**  
- Applicable across varied CCTV object-detection contexts  
- Filter detections by **specific classes** within polygon regions  
> **Extended use cases** – e.g., safety incidents prevention (region danger alerts),  
> class-specific detection analytics and data structuring

<!-- Video -->
https://github.com/user-attachments/assets/cf991294-5b1c-45b3-a008-12115700f62c

---

[![CCTV_POLIGON_프로젝트_상세보기](https://img.shields.io/badge/CCTV_POLIGON_프로젝트_상세보기-FF5722?style=for-the-badge&logo=gitbook&logoColor=white)](https://github.com/WhiteSnake-MrBBoo/information_portfolio/blob/main/docs/cctv-vision-dashboard.md)

---

### 3) UiPath Review Summarization Pipeline
**Stack:** UiPath, VB.NET Invoke Code, Newtonsoft JSON, Excel Activities  
**Key Features:**  
- Blind reviews → **Pros / Cons / Decision** (3-part summarization), auto schema build for **`Dt_Blind_Ai_Result`**  
- Safe parsing for `choices[0].message.content` / `text`, **MaxLength = -1**, write raw JSON to `Decision` on error  
- Bulk reviews → **Excel auto export** (WrapText, column width)

- Uses **ChatGPT (AI)** to analyze and infer reviews; yields target **decision outputs**

**Impact (examples):**  
- **Shorter analysis lead time** via RPA  
- **Semi-automated reporting** through AI-driven review analysis  
- Local EXCEL export for easy downstream analysis  
- Prompt presets & standardized pipeline

<!-- Video -->
https://github.com/user-attachments/assets/e8ea065c-bf0c-4f93-a32d-d476e298a9bf

---

[![RPA_기업리뷰_AI_SUMMARY_프로젝트_상세보기](https://img.shields.io/badge/RPA_기업리뷰_AI_SUMMARY_프로젝트_상세보기-0A66C2?style=for-the-badge&logo=openai&logoColor=white)](https://github.com/WhiteSnake-MrBBoo/information_portfolio/blob/main/docs/uipath-blind-review-pipeline.md)

---

### 4) Prompt-Driven AI Creative Pipeline 🎶🎥
**Stack:** Suno (AI Music), Sora (AI Video), Prompt Engineering, Python  

**Key Features:**  
- **Prompt-engineering–driven AI**  
  - *Suno* → generates **custom music** from lyrics/style/tempo  
  - *Sora* → **music video / animation** from text prompts  
- **Prompt experiments → output variations**  
  - Compare color tones, camera views, storyline patterns  
- **Pipeline documentation**  
  - Prompt → Output → Improvement logs → Templates

**Impact (examples):**  
- Single prompt → **Music + Video + Story** auto-generated  
- Accumulated prompt design patterns into **reusable templates**  
- Demonstrates **AI utilization = developer productivity/creativity boost**

<!-- Video -->
https://github.com/user-attachments/assets/3fa89729-0793-48db-9c92-9fe08368ddf7

---

## 🔗 Detailed Document for AI_Prompt MUSIC_VIDEO
[![AI_PROMPT_CREATIVE_PIPELINE](https://img.shields.io/badge/AI_PROMPT_CREATIVE_PIPELINE-8A2BE2?style=for-the-badge&logo=openai&logoColor=white)](https://github.com/WhiteSnake-MrBBoo/information_portfolio/blob/main/docs/ai-prompt-creative-pipeline.md)

---

## 🧰 Tech Stack
**Backend:** JAVA, Spring Boot 3.4, JDK 21, Thymeleaf, ModelMapper, JPA, MariaDB, AWS  
**Vision/ML:** Ultralytics YOLOv5–v11, OpenCV, RoboFlow, Python 3.x, Flask  
**RPA:** UiPath, VB.NET Invoke Code, Newtonsoft JSON, Excel Activities  
**Frontend:** Bootstrap 5, HTML5/CSS3/JS, jQuery/Ajax/Fetch  
**Generative AI:** Suno (AI Music), Sora (AI Video), Prompt Engineering  
**DevOps/Etc:** IntelliJ, GitHub, HeidiSQL, MobaXterm, Linux  

---

## 🧭 Design & Documentation
- Case studies include **Architecture / Sequence / ERD / Prompt Diagrams**  
- Common rules: Principal-based auth, ModelMapper patterns, logging format, CRUD naming, readability-first  
- **Errors / AI inference failures** surfaced up to the UI for transparency  
- **Prompt experiment logs** for result comparison and reproducibility

---

## 📄 Contact & Links
- 📧 Email: [mrbulsapabb@gmail.com](mailto:mrbulsapabb@gmail.com)  
- 🐙 GitHub: [WhiteSnake-MrBBoo](https://github.com/WhiteSnake-MrBBoo)  
- 📄 PPT / PDFs:
- [📄 (JAVA) SpringBoot SixthSense Hotel](./assets/SixthSense_hotel.pdf)  
- [📄 RPA Blind AI](./assets/RPA_Blind_AI.pdf)

