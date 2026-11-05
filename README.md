# SmartStay – Advanced Hostel Management System
### SHRIDEVI Degree College &bull; Kings and Queen Hostel

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.x-black.svg)](https://flask.palletsprojects.com/)
[![MySQL](https://img.shields.io/badge/Database-MySQL%20%2F%20XAMPP-orange.svg)](https://www.apachefriends.org/)
[![PyMySQL](https://img.shields.io/badge/Connector-PyMySQL%20(Pure%20Python)-green.svg)](https://pymysql.readthedocs.io/)
[![Zero-Compilers](https://img.shields.io/badge/C%2B%2B%20%2F%20Node.js-None%20Required-success.svg)](#technology-stack)

A modern, responsive, commercial-grade web-based Hostel Management System developed for **SHRIDEVI Degree College** to manage **Kings and Queen Hostel** (Kings Hostel for Boys & Queens Hostel for Girls).

---

## 👥 Assigned System Roles & Users (Exact Order)

The database and application have been updated with the exact configured roles and names:

### 1. Main Administrator
- **Name**: **Bhagya**
- **System ID**: `ADM0001`
- **Username**: `admin`
- **Password**: `Admin@123`
- **Designation**: Chief System Administrator, SHRIDEVI Degree College
- **Access**: Master control, staff approvals, warden management, permission governance, audit logs, financial reports.

### 2. Hostel Warden
- **Name**: **Parvathi**
- **System ID**: `WRD0001`
- **Username**: `parvathi`
- **Password**: `Warden@123`
- **Designation**: Hostel Warden, Kings and Queen Hostel
- **Access**: Operational authority over room allocation, student check-in, leave/complaints approval.

### 3. Hostel Staff
- **Name**: **Bhargavi**
- **System ID**: `STF0001`
- **Username**: `bhargavi`
- **Password**: `Staff@123`
- **Designation**: Hostel Operations Supervisor
- **Access**: Approved staff with full operations authority (student registration, bed allocation, manual fee recording, request processing).

### 4. Resident Students (In Exact Order)

| # | Student Name | System ID | Login Username | Password | Assigned Room & Hostel | Course |
|---|---|---|---|---|---|---|
| 1 | **Abhilasha** | `STU20260001` | `STU20260001` | `Student@123` | Room Q-101 (Queens Hostel / Girls) | BCA |
| 2 | **Harika** | `STU20260002` | `STU20260002` | `Student@123` | Room Q-101 (Queens Hostel / Roommate with Abhilasha) | BBA |
| 3 | **Chandan** | `STU20260003` | `STU20260003` | `Student@123` | Room K-101 (Kings Hostel / Boys) | B.Sc CS |
| 4 | **Santosh** | `STU20260004` | `STU20260004` | `Student@123` | Room K-101 (Kings Hostel / Roommate with Chandan) | B.Com |
| 5 | **Lekhan** | `STU20260005` | `STU20260005` | `Student@123` | Room K-102 (Kings Hostel / Boys) | BCA |
| 6 | **Yogi** | `STU20260006` | `STU20260006` | `Student@123` | Room K-102 (Kings Hostel / Roommate with Lekhan) | BBA |

---

## 🏢 Hostel Residential Blocks

1. **Kings Hostel (Boys Block) - SHRIDEVI Degree College**
   - Rooms: `K-101`, `K-102`, `K-201`, `K-202`
   - Resident Scholars: **Chandan**, **Santosh** (Room `K-101`), **Lekhan**, **Yogi** (Room `K-102`)
2. **Queens Hostel (Girls Block) - SHRIDEVI Degree College**
   - Rooms: `Q-101`, `Q-102`, `Q-201`, `Q-202`
   - Resident Scholars: **Abhilasha**, **Harika** (Room `Q-101` sharing)

---

## 🌟 Key Application Features

1. **Three Dedicated User Portals with Separate Logins & Dashboards**:
   - **Main Administrator Portal (`/admin/login`)**: Complete system authority managed by Bhagya.
   - **Staff & Warden Operations Portal (`/staff/login`)**: Operations console for Parvathi (Warden) and Bhargavi (Staff).
   - **Student Resident Portal (`/student/login`)**: Self-service portal for Abhilasha, Harika, Chandan, Santosh, Lekhan, Yogi.

2. **Automatic Collision-Free ID Generation**:
   - Admin ID: `ADM0001`
   - Warden ID: `WRD0001`
   - Staff ID: `STF0001`
   - Student ID: `STU20260001` ... `STU20260006`
   - Ticket Request ID: `REQ00001`
   - Payment Receipt ID: `REC20260001`

3. **Smart Room-Sharing Display**:
   - Abhilasha and Harika view each other as roommates in Room Q-101.
   - Chandan and Santosh view each other as roommates in Room K-101.
   - Lekhan and Yogi view each other as roommates in Room K-102.

4. **Fee Management & Manual Payment Receipts**:
   - Fee invoice and statement balance tracking in Indian Rupees (₹).
   - Instant receipt generation upon recording collections.

5. **Student Ticket System**:
   - Students can submit maintenance complaints and room-change petitions.
   - Staff and Warden can review tickets, add official remarks, and update status (`APPROVED`, `COMPLETED`, `REJECTED`).

---

## 🚀 Windows Execution Instructions

1. **Ensure MySQL is running in XAMPP** (Port 3306).
2. **Open PowerShell in the project directory**:
   ```powershell
   cd C:\Users\ADMIN\.gemini\antigravity\scratch\SmartStay
   ```
3. **Activate Virtual Environment**:
   ```powershell
   venv\Scripts\activate
   ```
4. **Run Application**:
   ```powershell
   python app.py
   ```
5. **Open Browser**:
   Navigate to **[http://127.0.0.1:5000](http://127.0.0.1:5000)**.

---

## 🧪 Automated Test Suite Output

```powershell
venv\Scripts\activate
python test_system.py
```
Output:
```text
.......
Ran 7 tests in 3.4s
OK
[PASS] 01: Landing page rendered with SHRIDEVI Degree College & Kings and Queen Hostel branding.
[PASS] 02: Admin authentication verified for Bhagya.
[PASS] 03: RBAC security verified (Student locked out of Admin & Staff portals).
[PASS] 04: Student room-sharing verified (Abhilasha and Harika in Room Q-101).
[PASS] 05: Student room-sharing verified (Chandan and Santosh in Room K-101).
[PASS] 06: Staff ticket review and approval workflow verified for Bhargavi.
[PASS] 07: Warden login verified for Parvathi.
```
