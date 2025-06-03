# Comp1168-Database Management-Group Project

**Group Size:** Maximum Six (6) students (may belong to different Lab groups/CRNs)  
**Due Date:** Sunday August 3, 2025  
(Submission through BrightSpace)  
(Three files per group: one PDF and two SQL script files as explained on page 6)

---

## Project Synopsis

ABC Walk-in Clinic is located in a large metropolitan city in Canada. The clinic staff consists of:
- Ten doctors
- Six nurses
- Five office secretaries
- Two administrative assistants
- One manager

First-time patients must visit the clinic in person and fill out a registration form containing their personal and health-related information. An office secretary then enters that information into the computer-based information system.

Patients may either become **permanent** (enrolled) patients for one of the doctors by filling out the necessary forms or continue as **walk-in** patients. Enrolled patients can book appointments online or by phone. A secretary then schedules an appointment with the appropriate doctor on a particular day and time. Any appointment that is canceled less than 24 hours in advance incurs a fifty-dollar fine.

During a visit, a patient reports to the secretary who either places them in the walk-in queue or, if an appointment exists, checks them in. A nurse then escorts the patient to an examination room, records their symptoms and medical issues, and, if needed, takes vital measurements (blood pressure, temperature, height, and weight) before entering all collected information into the system.

The clinic system should track appointment statuses (booked, canceled, arrived, checked in, checked out, LWT—left without treatment, No show, etc.). While healthcare is free in Canada (with the clinic reimbursed by the government), a small fee may be charged for services not covered (for example, for Sick notes or for visitors not under government health coverage).

Once the nurse completes the initial assessment, the doctor examines the patient, may order diagnostic tests (blood work, X-ray, ultrasound, etc.), and records the patient’s symptoms, diagnosis, and treatment (including prescriptions). The system is required to store all this information. Additionally, if a referral is made to a specialist, that information must also be documented.

After diagnostic results are received from the laboratory, a nurse reviews the reports and uploads them to the patient’s electronic file. In some cases, the nurse may also call the patient to arrange a follow-up appointment if necessary.

---

## Clinic Operations and Scheduling

The clinic operates in two six-hour shifts:
- **Shift 1:** 7 a.m. to 2 p.m.
- **Shift 2:** 2 p.m. to 8 p.m.

The Manager is responsible for scheduling doctors, nurses, and secretaries. While doctors are paid by the government, the Manager must handle the salary payments for all other employees based on their hours worked. The system should store the hours and enable the Manager to generate a bi-weekly report for calculating salaries (assuming reasonable hourly rates for nurses and secretaries).

---

## Project Requirements

Please make reasonable and educated assumptions about missing or ambiguous information and document your assumptions briefly.

1. **Conceptual Data Model:**  
   Create a conceptual data model using Draw.io (or similar software), including all entities and their relationships (incorporate any many-to-many (M:M) relationships).

2. **Physical (Logical) Data Model:**  
   Develop a physical (logical) data model using MySQL Workbench® based on your conceptual model.  
   - Create a new schema named `GroupxxSchema` (replace "xx" with your group number, e.g., `Group21Schema`).
   - Design a physical EER model that includes tables, appropriate columns, and one-to-many (1:M) relationships.
   - Assign proper data types and add appropriate keys and constraints.
   - Ensure all relationships are in Third Normal Form (3NF).

3. **Forward Engineering:**  
   Forward engineer your EER model to create the database tables and relationships. Insert 10–15 records per table.

4. **SQL Queries:**  
   Create the following ten (10) queries. For each query, copy the text (as provided below) along with its serial number as a comment before your SQL code:

   1. **Query 1:**  
      Create a query that returns patients' full names, addresses, phone numbers, and email addresses. (Minimum ten results required.)

   2. **Query 2:**  
      Create a query that lists the full names of all patients and their last appointment dates who have not had any appointment in the clinic in the last 2 years. (At least one patient required.)

   3. **Query 3:**  
      Create a query that returns all appointments for a specific patient in 2023. (At least five appointments needed; include patient names, examining doctors' and nurses' names, appointment dates/times, and tests ordered by the doctor.)

   4. **Query 4:**  
      Create a query that returns all appointments that were either canceled or where patients were marked as No Show in December 2023. (Minimum five results required.)

   5. **Query 5:**  
      Create a query that returns the names of staff members (excluding doctors), their hourly rates, number of hours worked, and salary (calculated column; assume there are 13 employees) for a two-week period.

   6. **Query 6:**  
      The Clinic Manager wants to send "Happy holidays" greeting cards in December and print mailing labels showing two columns—the concatenated full names and complete addresses (combining street address, city, province, and Postal Code). Create a query to retrieve this information.

   7. **Query 7:**  
      Create a query that returns all patients and their doctor's names for patients who have permanently enrolled with any doctor at the clinic.

   8. **Query 8:**  
      Create a query that returns a list of all patients along with their family members. Modify the patient table to include:
      - A column (`primary_member_id`) designating a primary member.
      - A column (`relationship`) to indicate the relationship (e.g., husband, wife, son, daughter).

   9. **Query 9:**  
      Create a query that generates a list of all patients seen by a particular doctor on a given date (for example, December 12, 2022).

   10. **Query 10:**  
       Create a query that returns the name of a patient who paid a fee to the clinic, along with the service for which the fee was paid and the doctor's name (e.g., "Dr. Smith, Sick Note").

---

## Project Submission Requirements

Each group must submit three (3) separate files via BrightSpace before the deadline:

1. **File No. 1 – Project Report (PDF):**  
   - **Cover Page:** All members' last names, first names, student IDs, and CRN.
   - **Page 2:** The Conceptual Data Model (created via Draw.io or similar, then inserted as an image).
   - **Page 3:** The Logical/Physical ER Model (created in MySQL Workbench or similar, then inserted as an image). *(See Appendix A for instructions.)*
   - **Page 4:** Any assumptions or clarifications.

2. **File No. 2 – SQL Script File for Schema:**  
   A script that creates the `GroupxxSchema` with the required tables and data. *(See Appendix B for instructions.)*

3. **File No. 3 – SQL Script File for Queries:**  
   A script containing the SQL code for the ten queries detailed above.

**Note:** Ten percent (10%) of marks are reserved for proper submission, organization, and formatting of your report as per the provided specifications.

---

Department

idDepartment INT DeptName VARCHAR(45) Indexes

Employee

idEmployee INT EmpName VARCHAR(45) fk_Employee_Department (Department_idDepartment INT) Indexes

## Appendix A: How to Export Models from MySQL Workbench as an Image

1. Open MySQL Workbench.
2. Navigate to `File` > `Export` > `Export as PNG...`
3. Ensure the following selections:
   - Local instance (e.g., MySQL57)
   - MySQL Model with the EER Diagram active
4. Useful keyboard shortcuts:
   - **New Model:** `Ctrl+N`
   - **Open Model:** `Ctrl+0`
   - **Save Model:** `Ctrl+S` (or `Ctrl+Shift+S` for "Save Model As...")
   - **Export Forward Engineer SQL CREATE Script:** `Ctrl+Shift+G`
5. Once the PNG is created, insert it into your Word document.  
   **Sample Diagram:**




---

## Appendix B: How to Script a Schema (Table Structure and Data)

1. **Access the Main Server Instance Page:**  
Click on `Administration` > `Management` > `Data Export`.

2. **Schema Export Options:**  
- Choose the schema to export.
- Check these options:
  - Dump Structure and Data.
  - Specify a script file name (e.g., `GroupxxSchema`) and select your desired path.
  - Create Dump in a Single Transaction.
  - Include Create Schema.

3. **Export Methods:**  
- **Option 1:** Export to Dump Project Folder  
  (Each table is exported into a separate file, allowing selective restoration, though this may be slower.)
- **Option 2:** Export to a Self-Contained File  
  (All objects are exported into one single file.)

4. **Finalize the Export:**  
- Ensure "Create Dump in a Single Transaction" is selected (for a self-contained file).
- Verify that "Include Create Schema" is checked.

---

*End of Document*
