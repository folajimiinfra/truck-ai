# **Technical Proposal: Truck Driver Assistance System**  

**Prepared by:** Aluko Folajimi O.
**Date:** 28/03/2025

---

![System Architecture Diagram](https://www.mermaidchart.com/raw/b9902e4a-7a5e-4ab7-8286-decf0d7cd7a1?theme=light&version=v0.1&format=svg) 


## **1. Introduction**  
This proposal outlines the development of an **AI-powered agentic tool** designed to help truck drivers quickly connect with nearby mechanics when facing vehicle issues. The system will reduce downtime, optimize repair workflows, and improve fleet management by integrating real-time location tracking, automated notifications, and a centralized dashboard.  

### **Key Objectives**  
✔ **Fast Mechanic Matching** – AI finds the nearest available mechanic.  
✔ **Automated Notifications** – Instant SMS alerts via AWS.  
✔ **Centralized Dashboard** – Fleet managers track issues in real time.  
✔ **Cost & Time Savings** – Minimize truck downtime.  

---

## **2. Technology Stack**  
We propose a **high-performance, scalable** solution using:  

| Technology | Purpose | Why Chosen? |
|------------|---------|-------------|
| **NestJS** | Backend API | Robust framework for scalable server-side logic |
| **Prisma** | Database ORM | Type-safe, efficient PostgreSQL queries |
| **AWS (SNS, RDS)** | Cloud infrastructure | Reliable SMS & database hosting |
| **PostgreSQL + PostGIS** | Database | Advanced geospatial queries for mechanic matching |
| **Docker** | Containerization | Ensures consistent deployment |

---

## **3. System Architecture**  

### **3.1 Core Components**  
1. **Driver Issue Reporting**  
   - Mobile/web form to submit truck issues (type, description, location).  
   - GPS auto-capture for precise mechanic matching.  

2. **AI Mechanic Matching Engine**  
   - Uses **PostGIS** to find mechanics within a **50km radius**.  
   - Prioritizes availability and proximity.  

3. **AWS SNS Notifications**  
   - Automatically sends SMS alerts to mechanics.  
   - Confirms acceptance/rejection.  

4. **Fleet Manager Dashboard**  
   - Real-time issue tracking.  
   - Mechanic response monitoring.  



---

## **4. Detailed Implementation**  

### **4.1 Backend (NestJS)**  
- **RESTful API** for issue reporting, mechanic lookup, and status updates.  
- **Prisma ORM** ensures fast, type-safe database operations.  
- **JWT Authentication** for secure access.  

### **4.2 Database (PostgreSQL + PostGIS)**  
- **Optimized for geospatial queries** (e.g., "Find mechanics within 50km").  
- **Tables:**  
  - `Drivers` (Truck details, contact info)  
  - `Mechanics` (Location, availability, specialty)  
  - `Issues` (Status, repair history)  

### **4.3 AWS Integration**  
- **Amazon SNS** for SMS alerts (scalable & reliable).  
- **RDS PostgreSQL** for managed database hosting.  
- **Deployed via Docker** for consistency.  

---

## **5. Why This Approach?**  

| Requirement | My Solution | Benefit |
|-------------|--------------|---------|
| **Fast Mechanic Matching** | PostGIS geospatial queries | Finds mechanics in milliseconds |
| **Real-Time Notifications** | AWS SNS | Instant SMS alerts |
| **Scalability** | NestJS + Docker | Handles 1000s of requests |
| **Reliability** | AWS RDS | Auto-backups, high uptime |
| **Maintainability** | Prisma ORM | Clean, type-safe code |

---

## **6. Development Timeline**  
| Phase | Duration | Deliverables |
|-------|----------|-------------|
| **1. Setup & DB Design** | 3 days | PostgreSQL schema, Prisma models |
| **2. API Development** | 5 days | NestJS endpoints, AWS integration |
| **3. Notification System** | 3 days | SMS alerts via AWS SNS |
| **4. Testing & Deployment** | 3 days | Dockerized deployment on AWS |

**Total:** **2 weeks** (as requested)  

---

## **7. Cost Breakdown**  
| Item | Cost (₦) |
|------|---------|
| Backend (NestJS/Prisma) | 70,000 |
| AWS Setup (SNS, RDS) | 50,000 |
| Geospatial Logic (PostGIS) | 30,000 |
| **Total** | **₦150,000** (fixed) |

---

## **8. Next Steps**  
✅ **Client Approval** – Review & sign-off.  
✅ **Kickoff** – Database setup & API development.  
✅ **Testing** – Ensure mechanic matching works flawlessly.  
✅ **Deployment** – Go live on AWS.  

---  
**Prepared by:**  
Aluko Folajimi O.
09126669941 | folajimiopeyemisax13@gmail.com


---
