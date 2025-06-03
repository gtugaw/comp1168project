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

Please make reasonable and educated assumptions about missing or ambiguous information and document your
