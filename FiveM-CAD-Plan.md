# FiveM Multi-Department CAD System – Development Checklist

## 1️⃣ Planning & Architecture
- [ ] Define CAD purpose and scope
- [ ] Finalize supported departments:
  - [ ] LSPD
  - [ ] SASP
  - [ ] SAFR
  - [ ] Dispatch
  - [ ] DOJ
- [ ] Define core user flows per department
- [ ] Decide mono-repo vs split frontend/backend
- [ ] Choose hosting strategy
- [ ] Create high-level system diagram

---

## 2️⃣ Tech Stack & Framework Setup (Latest Versions)
- [ ] Initialize **Next.js (App Router + TypeScript)**
- [ ] Configure **Tailwind CSS**
- [ ] Configure ESLint & Prettier
- [ ] Set up environment variables
- [ ] Initialize Git repository
- [ ] Set up Docker (optional early)
- [ ] Create base folder structure

---

## 3️⃣ Authentication (Discord Login)
- [ ] Configure Discord Developer Application
- [ ] Implement Discord OAuth2 login
- [ ] Set up **Auth.js**
- [ ] Store Discord user ID
- [ ] Restrict login to main Discord server
- [ ] Fetch Discord roles on login
- [ ] Handle login errors & edge cases
- [ ] Implement logout

---

## 4️⃣ Role Mapping & Permission System
- [ ] Define department ↔ Discord role mapping
- [ ] Define permission levels:
  - [ ] LSPD
  - [ ] SASP
  - [ ] SAFR
  - [ ] Dispatch
  - [ ] DOJ
  - [ ] Admin
- [ ] Create permission utility
- [ ] Implement middleware for page protection
- [ ] Implement API route protection
- [ ] Deny access UI for unauthorized users

---

## 5️⃣ Database & ORM Setup
- [ ] Set up **PostgreSQL**
- [ ] Initialize **Prisma**
- [ ] Design core schema:
  - [ ] Users
  - [ ] Departments
  - [ ] Units
  - [ ] Calls
  - [ ] Reports
  - [ ] Citizens
  - [ ] Vehicles
- [ ] Run initial migrations
- [ ] Seed development data

---

## 6️⃣ Base Layout & Navigation
- [ ] Create global layout
- [ ] Implement sidebar navigation
- [ ] Show/hide pages by role
- [ ] Create department-based routing
- [ ] Create dashboard shell pages
- [ ] Add dark/light theme support
- [ ] Implement notification system

---

## 7️⃣ Core Dispatch System (FIRST FUNCTIONAL FEATURE)
- [ ] Dispatch dashboard
- [ ] Call creation form
- [ ] Call priority levels
- [ ] Active calls list
- [ ] Call status tracking
- [ ] Assign units to calls
- [ ] Dispatch notes
- [ ] Cross-department call visibility

---

## 8️⃣ Unit Management
- [ ] Unit creation system
- [ ] Unit status tracking (10-8, 10-6, etc.)
- [ ] Unit ↔ call linking
- [ ] Unit availability logic
- [ ] Live unit list per department

---

## 9️⃣ LSPD / SASP Features
- [ ] PD dashboard
- [ ] View assigned calls
- [ ] Incident report creation
- [ ] Arrest reports
- [ ] Citations
- [ ] BOLO system
- [ ] Warrant records
- [ ] Search PD records

---

## 🔟 SAFR (EMS / Fire) Features
- [ ] SAFR dashboard
- [ ] Medical report creation
- [ ] Fire report creation
- [ ] Patient transport logs
- [ ] View & accept calls
- [ ] SAFR unit management

---

## 1️⃣1️⃣ DOJ Access & Case Review
- [ ] DOJ dashboard
- [ ] Read-only access enforcement
- [ ] View PD reports
- [ ] View EMS reports
- [ ] Case linking system
- [ ] Search & filter cases

---

## 1️⃣2️⃣ Records & Databases
- [ ] Citizen database
- [ ] Vehicle database
- [ ] Name & plate search
- [ ] Report cross-linking
- [ ] Record history tracking
- [ ] Audit logging

---

## 1️⃣3️⃣ Real-Time Features
- [ ] WebSocket / Socket.IO setup
- [ ] Live call updates
- [ ] Live unit status updates
- [ ] Dispatch instant refresh
- [ ] Notification push system

---

## 1️⃣4️⃣ Security & Hardening
- [ ] Secure API endpoints
- [ ] CSRF protection
- [ ] Rate limiting
- [ ] Input validation
- [ ] Permission re-checks
- [ ] Activity logging

---

## 1️⃣5️⃣ FiveM Integration (Final Phase)
- [ ] FiveM server resource setup
- [ ] Secure CAD API key
- [ ] Sync in-game unit status
- [ ] Create calls from in-game 911
- [ ] Player ↔ CAD user linking
- [ ] Character data syncing
- [ ] Discord webhooks for logs

---

## 1️⃣6️⃣ Testing & Deployment
- [ ] Role-based access testing
- [ ] Dispatch stress testing
- [ ] UI/UX review per department
- [ ] Performance optimization
- [ ] Production build
- [ ] Deployment to hosting platform
- [ ] Environment hardening

---

## 1️⃣7️⃣ Future Enhancements (Post-Launch)
- [ ] Live GPS map
- [ ] MDT mobile view
- [ ] Penal code system
- [ ] Court case management
- [ ] Evidence uploads
- [ ] Multi-server support
