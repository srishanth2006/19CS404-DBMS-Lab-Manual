# Experiment 1: Entity-Relationship (ER) Diagram

## 🌟 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.  
- Students have admission number, name, DOB, contact info.  
- Instructors with staff number, contact info, etc.  
- Courses have number, name, credits.  
- Track course enrollments by students and enrollment date.  
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.  
- Doctors and their departments, contact info, specialization.  
- Appointments with reason, time, patient-doctor link.  
- Medical records with treatments, diagnosis, test results.  
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.  
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).  
3. Include:  
   - Cardinality & participation constraints  
   - Prerequisites for University OR Billing for Hospital  
4. Explain:  
   - Why you chose the entities and relationships.  
   - How you modeled prerequisites or billing.  

---

# ER Diagram Submission - Student Name

### Scenario Chosen:
**Hospital**

### ER Diagram:
**HOSPITAL DATABASE:**  
![Screenshot 2025-05-12 081436](https://github.com/user-attachments/assets/7f377a86-f23e-424d-8478-f48081fbdbd8)

---

### Entities and Attributes:

- **Patient**: Name, Phone Number, Address, Insurance Company  
- **Doctor**: Name, Hospital ID, Specialization, Department  
- **Nurse**: Name, Hospital ID  
- **Receptionist**: Entry & Exit Time  
- **Pharmacy**: Medicine Name, Medicine Type, DOM, DOE  
- **Rooms**: RNO, Floor  
- **Records**: Record No, Date  

---

### Relationships and Constraints:

- **Allocated To** between *Patient* and *Rooms*  
  - Cardinality: One-to-One  
  - Participation: Total on patient  

- **Consults** between *Patient* and *Doctor*  
  - Cardinality: Many-to-Many  
  - Participation: Partial  

- **Guides** between *Nurse* and *Patient*  
  - Cardinality: One-to-Many  
  - Participation: Partial  

- **Instructs** between *Doctor* and *Nurse*  
  - Cardinality: One-to-Many  
  - Participation: Partial  

- **Maintains** between *Receptionist* and *Records*  
  - Cardinality: One-to-Many  
  - Participation: Total on records  

- **Purchase Medicines** between *Patient* and *Pharmacy*  
  - Cardinality: One-to-Many  
  - Participation: Partial  

---

### Extension (Billing):

The billing aspect is indirectly modeled through the **"Purchase Medicines"** relationship between the **Patient** and **Pharmacy**, where details such as **DOM (Date of Manufacture)** and **DOE (Date of Expiry)** are tracked. This implies billing and inventory tracking. Additionally, doctor consultations and room allocations are billable services implicitly modeled in the relationships.

---

### Design Choices:

Entities were selected based on real-world hospital workflow components: patients, rooms, doctors, nurses, pharmacists, and receptionists. Relationships like *consults*, *guides*, *instructs*, and *allocated to* reflect real interactions and responsibilities.  
Billing was incorporated through the pharmacy-patient connection and service interactions. Cardinality and participation were based on logical constraints (e.g., a patient is allocated one room, but a doctor can consult many patients).

---

### RESULT

Successfully completed the ER diagram for the hospital database scenario, including all necessary entities, relationships, attributes, constraints, and billing logic as required.

