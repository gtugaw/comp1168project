Here's a structured Markdown version of the **Comp1168-Project(ABC Walk-in Clinic)** document. You can save it as a `.md` file for easy readability and formatting in Markdown-supported editors.

```markdown
# Comp1168-Database Management-Group Project

**Group Size:** Maximum Six (6) students (may belong to different Lab groups/CRNs)  
**Due Date:** Sunday August 3, 2025  
(Submission through BrightSpace)  
(Three files per group: one PDF and two SQL script files as explained on page 6)

---

## Project Synopsis

ABC Walk-in Clinic is located in a large metropolitan city in Canada. The clinic staff consists of:
- **Ten doctors**
- **Six nurses**
- **Five office secretaries**
- **Two administrative assistants**
- **One manager**

First-time patients must visit the clinic in person and fill out a registration form containing personal and health-related information. An office secretary enters this information into the computer-based system.

### Patient Types:
- **Permanent Patients (Enrolled)**: Patients can register with a specific doctor and book appointments online or via phone.
- **Walk-in Patients**: These patients do not have a dedicated doctor and visit as needed.

### Appointment Process:
1. **Booking**: Secretaries schedule appointments for enrolled patients.
2. **Cancellation Policy**: Appointments canceled less than **24 hours in advance** incur a **$50 fine**.
3. **Check-in Process**:
   - Walk-in patients enter a queue.
   - Enrolled patients check in for their scheduled appointments.
4. **Examination Steps**:
   - A nurse takes the patient to an exam room.
   - Records symptoms and vital signs (blood pressure, temperature, height, weight).
   - Inputs all collected data into the system.

### Clinic System Features:
- Tracks appointment statuses: **Booked, Canceled, Arrived, Checked-in, Checked-out, LWT (Left Without Treatment), No Show**.
- Manages **billing** for non-covered services (e.g., sick notes, visitor fees).
- Doctors enter **diagnoses, treatments, prescriptions**, and can refer patients to specialists.
- Nurses **review diagnostic results**, update records, and schedule follow-ups.

---

## Clinic Operations and Scheduling

### Shifts:
- **Shift 1:** 7 a.m. – 2 p.m.
- **Shift 2:** 2 p.m. – 8 p.m.

### Staff Payments:
- **Doctors** are paid by the government.
- **Other employees (nurses, secretaries, assistants)** receive salaries based on **worked hours**.
- The **Manager** oversees payroll and generates **bi-weekly salary reports**.

---

## Project Requirements

### Data Models:
1. **Conceptual Model**  
   - Create an entity-relationship diagram (**ERD**) using Draw.io.  
   - Define **entities and relationships**, including **many-to-many (M:M) relationships**.

2. **Physical Data Model (Logical Model)**  
   - Build an **EER model** in **MySQL Workbench** using the schema `GroupxxSchema` (replace “xx” with your group number).  
   - Ensure **Third Normal Form (3NF)** compliance.  
   - Define **columns, keys, constraints, and relationships (resolved to 1:M)**.

3. **Forward Engineering**  
   - Convert EER model into **physical tables** using MySQL Workbench.  
   - Insert **10–15 sample records per table**.

---

## Required SQL Queries

Each query must be **commented** with its description.

```sql
-- Query 1: Retrieve Patients' full names, addresses, phone numbers, and emails.
```

```sql
-- Query 2: List patients who have not had an appointment in the last 2 years.
```

```sql
-- Query 3: Retrieve all appointments for a specific patient in 2023.
```

```sql
-- Query 4: Retrieve all canceled or No Show appointments from December 2023.
```

```sql
-- Query 5: Retrieve staff members (excluding doctors) with hours worked, hourly rates, and calculated salaries.
```

```sql
-- Query 6: Generate mailing labels for holiday greeting cards (full name + address).
```

```sql
-- Query 7: List enrolled patients along with their assigned doctors.
```

```sql
-- Query 8: Create a family member structure (add primary_member_id and relationship columns).
```

```sql
-- Query 9: Retrieve all patients seen by a specific doctor on a given date.
```

```sql
-- Query 10: Retrieve the name of a patient who paid a fee along with service details and doctor's name.
```

---

## Submission Guidelines

Each group must submit **three (3) separate files** via BrightSpace:

1. **Project Report (PDF)**
   - **Cover Page:** Student names, IDs, CRN.
   - **Page 2:** Conceptual Data Model (Insert ERD image).
   - **Page 3:** Logical/Physical EER Model (Insert Workbench image).
   - **Page 4:** Assumptions & Clarifications.

2. **SQL Script for Schema Creation**
   - Script defining the **GroupxxSchema**, tables, relationships, and sample data.

3. **SQL Script for Queries**
   - Script containing all **ten SQL queries**.

*Note:* **10% of marks** are reserved for **proper formatting, submission, and organization**.

---

## Appendix A: Exporting Models as Images in MySQL Workbench

1. **Go to**: `File` > `Export` > `Export as PNG`
2. **Ensure selections**:
   - MySQL Model with **EER Diagram active**.
   - Choose the appropriate **database instance**.
3. **Keyboard Shortcuts**:
   - **New Model:** `Ctrl+N`
   - **Open Model:** `Ctrl+O`
   - **Save Model:** `Ctrl+S`
   - **Export as SQL:** `Ctrl+Shift+G`
   - **Export as PNG:** `Ctrl+Shift+P`

---

## Appendix B: Exporting Schema and Data

1. **Go to**: `Administration` > `Management` > `Data Export`
2. **Select schema** and enable:
   - **Dump Structure and Data**
   - **Include Create Schema**
   - **Create Dump in a Single Transaction**
3. **Export Formats**:
   - **Dump Project Folder** (individual table files)
   - **Self-contained File** (entire schema and data in one file)

---

### End of Document
```

You can copy and paste this into any Markdown-compatible editor! Let me know if you need any tweaks. 🚀
