# Authorized-Security-Testing-Lab
# 🔐 Authorized Security Testing Lab

> **Authorized • Isolated • Intentionally Vulnerable Security Testing Environment**

A controlled cybersecurity laboratory designed for security assessment practice, threat modeling, vulnerability validation, evidence collection, and professional security reporting.

---

## 📌 Project Overview

This repository documents an **authorized and isolated security testing laboratory** containing intentionally vulnerable systems.

The lab is designed to provide a safe environment for practicing:

- Web application security testing
- Network security assessment
- Vulnerability identification and validation
- Threat modeling
- STRIDE analysis
- Security evidence collection
- Risk assessment
- Security documentation and reporting
- Defensive security learning

All testing activities are restricted to the assets explicitly listed in the approved asset inventory.

> ⚠️ **Important:** This laboratory is intended only for authorized security testing. Do not apply the techniques documented here to systems that you do not own or have explicit permission to test.

---

## 🎯 Objectives

The primary objectives of this project are to:

1. Establish a clearly defined security testing scope.
2. Identify and document authorized laboratory assets.
3. Map trust boundaries and data flows.
4. Identify application and network attack surfaces.
5. Develop a STRIDE-based threat model.
6. Perform controlled, non-destructive security validation.
7. Collect minimum necessary evidence.
8. Document security findings professionally.
9. Recommend appropriate remediation measures.
10. Maintain clear rules of engagement throughout testing.

---

# 📋 Lab Information

| Field | Details |
|---|---|
| **Project Name** | Authorized Security Testing Lab |
| **Environment** | Isolated, intentionally vulnerable laboratory |
| **Lab Owner** | RabTech lab |
| **Security Assessor** | R. Aravinth |
| **Document Version** | 1.0 |
| **Approval Date** | September 2026 |
| **Purpose** | Security assessment, threat modeling, validation, and reporting |

---

# 🏗️ Lab Architecture

The laboratory consists of two authorized assets.

| Asset ID | Asset | Address | Environment | Scope |
|---|---|---|---|---|
| **LAB-01** | Local Training Web Application | `127.0.0.1:8080` | Local Lab | ✅ In Scope |
| **LAB-02** | Deliberately Vulnerable VM | `192.168.56.20` | Isolated Lab | ✅ In Scope |

---

# 🖥️ Asset Inventory

## LAB-01 — Local Training Web Application

| Field | Value |
|---|---|
| **Asset ID** | LAB-01 |
| **Type** | Web Application |
| **Address** | `127.0.0.1:8080` |
| **Environment** | Local Lab |
| **Owner** | RabTech lab |
| **Data** | Test / Training Data |
| **Primary Attack Surface** | Web interface and application inputs |
| **Scope** | In Scope |

### Assessment Areas

- Authentication and login controls
- Session management
- Application inputs
- URL parameters
- Authorization controls
- File upload functionality, if present
- API functionality, if present
- Input validation
- Error handling

---

## LAB-02 — Deliberately Vulnerable VM

| Field | Value |
|---|---|
| **Asset ID** | LAB-02 |
| **Type** | Virtual Machine |
| **Address** | `192.168.56.20` |
| **Environment** | Isolated Lab |
| **Owner** | RabTech lab |
| **Data** | Test / Training Data |
| **Primary Attack Surface** | Network services and applications |
| **Scope** | In Scope |

### Assessment Areas

- Network service exposure
- Service configuration
- Authentication controls
- Access controls
- Installed applications
- Security configuration
- Privilege boundaries

---

# 🌐 Trust Boundary

The authorized laboratory boundary separates the testing environment from all external and unauthorized systems.

```text
                         TESTER
                            |
                            |
                            v
              +---------------------------+
              |   AUTHORIZED LAB          |
              |        BOUNDARY            |
              |                           |
              |  +---------------------+  |
              |  |       LAB-01        |  |
              |  | Web Application     |  |
              |  | 127.0.0.1:8080      |  |
              |  +---------------------+  |
              |                           |
              |  +---------------------+  |
              |  |       LAB-02        |  |
              |  | Vulnerable VM       |  |
              |  | 192.168.56.20       |  |
              |  +---------------------+  |
              +---------------------------+
                            |
                            X
                    OUTSIDE LAB SCOPE
