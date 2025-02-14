# 🏥 **Appointment Management Domain**

## 📖 Description
The **Appointment Management** domain handles the scheduling and management of appointments for patients and doctors. The domain consists of independent microservices that allow the system to scale and maintain modularity. Each microservice is responsible for a different CRUD operation related to appointments, including create, read, update, and delete.

---

## 🔹 Microservices

### 📅 **1. Create Appointment**
- **📌 Description:** This microservice handles the creation of new appointments within the system.
- **🔹 Method:** `POST`
- **🔗 Dependencies:** Doctor, Patient, and Appointment database 🗄️
- **📥 Inputs:** Patient ID, Doctor ID, Appointment date and time
- **📤 Outputs:** Confirmation of appointment creation and appointment details 📅

### 🗓️ **2. Read Appointment**
- **📌 Description:** This microservice retrieves appointment details by appointment ID.
- **🔹 Method:** `GET`
- **🔗 Dependencies:** Appointment database 🗄️
- **📥 Inputs:** Appointment ID
- **📤 Outputs:** Appointment details such as date, time, patient, and doctor info 🧑‍⚕️

### 🔄 **3. Update Appointment**
- **📌 Description:** This microservice updates existing appointment details, such as rescheduling or modifying the patient/doctor information.
- **🔹 Method:** `PUT`
- **🔗 Dependencies:** Appointment database 🗄️
- **📥 Inputs:** Appointment ID, updated appointment details
- **📤 Outputs:** Confirmation of appointment update and new appointment details 🕓

### ❌ **4. Delete Appointment**
- **📌 Description:** This microservice deletes an appointment from the system.
- **🔹 Method:** `DELETE`
- **🔗 Dependencies:** Appointment database 🗄️
- **📥 Inputs:** Appointment ID
- **📤 Outputs:** Confirmation of appointment deletion 🗑️

---

## 🛠️ **Technologies Used**
- **⚙️ Backend:** Java, Spring Boot, Maven 💻
- **🗄️ Database:** PostgreSQL 🐘, MySQL 🐬

---

## 🔗 **Integrations**
- **🏥 Patient Management Domain:** Patients are associated with appointments, requiring interactions for creating, updating, and viewing appointments.
- **🩺 Doctor Management Domain:** Doctors' schedules are affected by appointment management, ensuring availability.
- **🧑 Admin Management Domain:** Administrators can manage appointments as part of their administrative duties.

---

## 📁 **Directory Structure**

```plaintext
└── davidsebas20-domain-appointment-management/
    ├── README.md
    ├── ms-createappointment/
    ├── ms-deleteappointment/
    ├── ms-readappointment/
    ├── ms-updateappointment/
    └── .github/
        └── workflows/
            └── deploy.yml



