# Streamlining Ticket Assignment for Efficient Support Operations

## 📌 Project Overview
At **ABC Corporation**, the increasing volume of support requests highlighted the need for a more efficient and automated ticket management process. Manual assignment often caused **delays, misrouting, and uneven workload distribution** across teams.  

This project leverages **ServiceNow** to implement an **automated ticket assignment system**, ensuring tickets are routed to the correct team without manual intervention.  

---

## 🎯 Project Objectives
- Automate ticket routing to ensure accurate and timely assignment.  
- Reduce delays in issue resolution by minimizing manual errors.  
- Improve customer satisfaction through faster response times.  
- Optimize resource utilization by balancing workloads.  
- Enhance transparency with clear assignment logic and reporting.  

---

## ✨ Key Features
- **Automated Routing** – Tickets go to the right team instantly.  
- **Dynamic Rules** – Configurable logic based on category or priority.  
- **Load Balancing** – Even distribution of workload.  
- **Escalation Support** – Auto-escalation for SLA breaches.  
- **Notifications** – Real-time alerts for quicker response.  
- **Analytics** – Reports on ticket flow and team performance.  

---

## ⚙️ ServiceNow Developer Setup
1. Create a free developer account at [ServiceNow Developer Portal](https://developer.servicenow.com/dev.do).  
2. Verify your email and log in.  
3. Request a **Personal Developer Instance (PDI)**.  
4. Use **Creator Studio/App Engine Studio** to build the application.
<img width="1885" height="772" alt="image" src="https://github.com/user-attachments/assets/1ca2c62f-6ac8-4eb1-b209-d5cab7f9ec52" />


---

## 🛠️ Project Implementation
The project was implemented in ServiceNow with the following components:  

### 1. Creating Users  
Users represent individuals in the system. Two users were created:  
- **Katherine Pierce** – Member of the Certificates Group.  
- **Manne Niranjan** – Member of the Platform Group.
<img width="1392" height="678" alt="user_record" src="https://github.com/user-attachments/assets/5a55f5dc-c0b7-4224-bac8-a3d19be405db" />


### 2. Creating Groups  
Groups represent teams that handle tickets:  
- **Certificates Group** – Handles certificate-related issues.  
- **Platform Group** – Handles login issues, 404 errors, and expired accounts.
<img width="1388" height="517" alt="group_record" src="https://github.com/user-attachments/assets/1407e7da-a505-447f-a150-c9bd326b5be0" />


### 3. Creating Roles  
Roles define permissions:  
- **Certificate_role** – Grants certificate issue handling access.  
- **Platform_role** – Grants platform issue handling access.
<img width="1413" height="466" alt="role_record" src="https://github.com/user-attachments/assets/966132c5-1676-4a47-b93f-3d665faaac66" />


### 4. Creating Table & Choices  
A custom table **Operations related** was created with fields:  
- Issue, Description, Assigned To, Status.  

Choices for the **Issue field**:  
- Unable to login to platform  
- 404 error  
- Regarding certificates  
- Regarding user expired
<img width="1367" height="727" alt="columns" src="https://github.com/user-attachments/assets/b3245d8a-82bb-4a5c-8f37-57dda4647ade" />


### 5. Assigning Users & Roles to Groups  
- **Certificates Group:** Katherine Pierce + Certificate_role  
- **Platform Group:** Manne Niranjan + Platform_role
<img width="1327" height="757" alt="assign_cert" src="https://github.com/user-attachments/assets/b6395051-2a53-4678-b766-be511487fe3c" />


### 6. Assigning Roles to Table  
Both **Certificate_role** and **Platform_role** were assigned **Read/Write access** to the *Operations related* table. 
<img width="1372" height="482" alt="access_write" src="https://github.com/user-attachments/assets/3ec982de-1231-4140-9f04-1db1b8fb1366" />


### 7. Creating ACLs  
Access Control Lists (ACLs) were defined for sensitive fields (e.g., Issue, Priority, Ticket Raised Date) to restrict access to authorized roles (admin).  
<img width="1390" height="480" alt="acl" src="https://github.com/user-attachments/assets/0422dc59-470a-4677-b1d6-e89ba3708212" />


### 8. Creating Flows for Ticket Assignment  
- **Flow 1:** Assign *“Regarding Certificates”* tickets to the Certificates Group.  
- **Flow 2:** Assign *Platform-related issues* (Login, 404 Error, User Expired) to the Platform Group.
<img width="1887" height="832" alt="image" src="https://github.com/user-attachments/assets/59f2f193-7b1d-4730-854e-97042694890b" />

  

## ✅ Conclusion
The implementation of the automated ticket assignment system at ABC Corporation has significantly improved IT support operations.  

By automating ticket routing in ServiceNow, the organization has:  
- **Reduced delays** by eliminating manual routing.  
- **Improved accuracy** by ensuring tickets always reach the right team.  
- **Optimized efficiency** through balanced workloads.  
- **Enhanced customer satisfaction** with faster issue resolution.  

This project demonstrates how **ServiceNow automation** can transform IT Service Management (ITSM) by minimizing administrative tasks and allowing support teams to focus on solving problems rather than managing ticket distribution.

---  
