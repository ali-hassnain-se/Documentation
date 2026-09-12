# System Design & UML Modeling Setup Guide

This guide details the complete local workstation setup for **System Design & Software Architecture** coursework, assignments, and architectural diagrams using **draw.io Desktop**.

---

## 1. Overview & Tool Choice

When working on Software Design and Architecture, having an offline, license-free, and high-fidelity diagramming environment is critical. While tools like StarUML are widely referenced in academia, free evaluation modes place watermarks on exports and feature trial prompts. 

**draw.io Desktop** (by JGraph) is chosen because:
- **100% Free & Open-Source:** No trial prompts, expiration dates, or watermarked exports.
- **Offline & Local-First:** Runs completely offline without internet dependencies or security firewall prompts.
- **Standards Compliant:** Native support for UML 2.5, Entity-Relationship (ERD), C4 Model, Flowcharts, and Cloud Architecture diagrams.
- **Git Friendly:** Saves raw diagrams as readable XML (`.drawio`), allowing clean version control, branch tracking, and SVG/PNG rendering inside GitHub repositories.

---

## 2. Installation & Verification

### Prerequisites
- **Operating System:** Windows 10 / 11 (64-bit)
- **Privileges:** Standard user access (no specialized network privileges required)

### Step-by-Step Installation
1. **Download the Official Installer:**
   - Source: [draw.io Desktop Releases (GitHub)](https://github.com/jgraph/drawio-desktop/releases/latest)
   - Asset: `draw.io-<version>-windows-installer.exe` (e.g., `draw.io-31.4.5-windows-installer.exe`).
2. **Execute Setup:**
   - Launch the downloaded `.exe` file.
   - Follow standard setup prompts (Default directory: `C:\Program Files\draw.io`).
3. **Launch the Application:**
   - Open **draw.io** from the Windows Start Menu or Desktop shortcut.
   - Select **Create New Diagram** → choose **Blank Diagram** → click **Create**.

---

## 3. Configuring Diagram Libraries

By default, draw.io loads general drawing shapes. To enable software engineering and architecture standard libraries:

1. Look at the lower-left corner of the interface and click **`+ More Shapes`**.
2. Under the **Software** section, enable:
   - `[x] UML` & `[x] UML 2.5`: Standard shapes for Class, Use Case, Sequence, Activity, and State Machine diagrams.
   - `[x] Entity Relation`: Database schema and ERD cardinality notations (Crow's Foot, Chen notation).
3. *(Optional)* Under **Networking** / **Software**, check:
   - `[x] C4`: Modern system architecture diagrams (Context, Container, Component, Code).
4. Ensure **Remember this setting** is checked, then click **Apply**.

---

## 4. Architectural Modeling Standards

### Key UML Elements Reference
| Diagram Type | Common Shapes & Connectors | Primary Purpose |
| :--- | :--- | :--- |
| **Class Diagram** | Class Box (Name, Attributes, Methods), Interface, Generalization (Inheritance), Association, Composition, Aggregation | Low-Level Design (LLD) & Object-Oriented Modeling |
| **Use Case Diagram**| Actor (Stick figure), Use Case (Oval), System Boundary, `<<include>>`, `<<extend>>` | Functional requirement scope & user interactions |
| **Sequence Diagram** | Lifeline, Activation Box, Synchronous Message (→), Asynchronous Message, Return Message (-->) | Runtime interactions and method call order between components |
| **ER Diagram (ERD)** | Table entity, Primary Key (`PK`), Foreign Key (`FK`), 1:1, 1:N, M:N Crow's Foot relations | Database structural modeling |

---

## 5. Exporting & GitHub Workflow

### Recommended Export Formats
- **For README / Documentation:** 
  - Go to `File` → `Export as` → `PNG` or `SVG`.
  - Check **Include a copy of my diagram** (allows reopening and editing directly from the exported image file).
  - Select **Transparent Background** for seamless display in GitHub dark/light themes.
- **For Academic Submissions:** 
  - Go to `File` → `Export as` → `PDF`.

### Recommended Repository Directory Structure

```text
Documentation/
├── MySQL/
│   └── MY-SQL-Setup.md                               # Database setup and reference docs
├── README.md                               # Technical Documentation Vault index
└── SYSTEM_DESIGN_SETUP.md                  # This setup guide & environment workflow
```
