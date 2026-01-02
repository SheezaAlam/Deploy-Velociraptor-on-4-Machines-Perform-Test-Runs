# **Velociraptor Deployment & Endpoint DFIR – Task 02**

## **Overview**

This repository contains the **Task 02 report** documenting the deployment, configuration, and testing of **Velociraptor** as an endpoint monitoring and Digital Forensics & Incident Response (DFIR) tool. The work was conducted as part of a **cybersecurity internship and hands-on lab practice**, focusing on endpoint visibility, remote command execution, and detection of simulated malicious behavior in a controlled environment.

---

## **Objective**

The primary objective of this task was to:

* Deploy Velociraptor on multiple Windows endpoints
* Verify successful client–server communication
* Execute commands remotely using Velociraptor hunts
* Simulate safe, non-destructive malicious behaviors
* Validate Velociraptor’s ability to log, detect, and collect forensic artifacts

---

## **Lab Environment**

* **Velociraptor Server:** Hosted and accessed via web-based console
* **Clients:** 4 Windows machines
* **Platform:** Virtualized lab environment
* **Access:** Velociraptor GUI for client management, hunts, and artifact collection

---

## **Task Breakdown**

### **1. Velociraptor Server Setup**

* Initialized and launched Velociraptor server successfully
* Accessed the web-based Velociraptor console
* Verified availability of:

  * Client management
  * Hunt execution
  * Server and client artifacts
  * Logs and collected results

---

### **2. Client Deployment on Windows Machines**

* Installed Velociraptor clients on four Windows endpoints
* Configured each client with the correct server address
* Started clients as system services
* Confirmed stable client–server communication through the console

---

### **3. Remote Command Execution Test (Hunt Execution)**

**Artifacts Used**

* `Windows.System.CmdShell`

**Commands Executed**

* `whoami`
* `ipconfig`

**Results**

* Commands executed successfully on all endpoints
* Outputs returned to the Velociraptor console
* Flow IDs generated for each execution
* Execution details and timestamps logged

**Conclusion**
This confirmed correct remote execution capability, reliable client response, and proper output collection.

---

### **4. Simulated Malicious Behavior Detection**

#### **4.1 Fake Malware File Creation**

* Created a fake malware-like executable with a system-like name (safe simulation)

**Artifact Used**

* `Windows.Search.FileFinder`

**Results**

* File successfully detected and uploaded
* MD5, SHA1, and SHA256 hashes calculated
* File metadata and timestamps collected

**Conclusion**
Velociraptor demonstrated effective file discovery and artifact collection.

---

#### **4.2 Suspicious PowerShell Execution**

* Executed a benign PowerShell command (`Get-Date`) encoded in Base64

**Detection**

* Logged under `Windows.System.Powershell`
* Flow ID generated
* Execution parameters and timestamps recorded

**Conclusion**
Although harmless, the activity simulated attacker techniques, and Velociraptor correctly logged and captured the behavior.

---

#### **4.3 Registry Run Key Persistence Simulation**

* Added a benign registry Run key manually to simulate persistence
* Verified creation using Registry Editor

**Conclusion**
Velociraptor detected registry changes, validating its ability to monitor persistence mechanisms.

---

## **Final Conclusion**

This task successfully demonstrated the practical use of **Velociraptor as an endpoint monitoring and DFIR tool**. All Windows endpoints connected correctly to the server, and remote command execution was verified. Simulated malicious activities—including file-based threats, encoded PowerShell execution, and registry persistence—were accurately logged and captured through artifacts and hunts.

The results confirm that the environment is correctly configured and capable of supporting **real-world security monitoring, threat detection, and forensic investigations**.

---

## **Files**

* `velociraptor_report_sheeza_alam_kahn.pdf` – Detailed Task 02 report with screenshots and analysis

---

## **Author**

**Sheeza Alam Khan**
BS Computer Science (Final Year)
