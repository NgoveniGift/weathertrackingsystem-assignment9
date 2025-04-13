
# 📘 Assignment 9: Domain Model and Class Diagram - Weather Tracking System

This repository contains the Domain Model, UML Class Diagram, and Reflection for the Weather Tracking System project.

## 🧱 Domain Model
The domain model outlines the core entities in the system, their attributes, methods, relationships, and business rules. These form the conceptual framework for designing the system’s database schema and class architecture.

📄 See: [Domain Model Table](#1-domain-model-table)

## 📊 UML Class Diagram
A UML class diagram built with Mermaid.js syntax displays the key entities, methods, attributes, and relationships (including multiplicities and navigability).

🛠️ Render in Mermaid-supported tools or Markdown viewers.

📄 See: [UML Class Diagram](#2-uml-class-diagram-mermaidjs)

## 🪞 Reflection
Covers:
- Granularity challenges
- Connections to Assignments 4, 6, and 8
- Comparison of object models vs. activity diagrams
- Lessons learned in object-oriented modeling

📄 See: [Reflection](#3-reflection-20-marks)

---

## ✅ Summary of Key Entities
- `UserAccount`: Manages user access and links to forecasts & locations
- `Location`: Tied to weather data and user tracking
- `Sensor`: Gathers raw weather data from environment
- `WeatherStation`: Controls and maintains sensor functionality
- `WeatherReport`: Compiled from sensor data
- `ForecastRequest`: User-initiated or automated forecast generator
- `Alert`: Sends emergency notifications for extreme conditions

---

## 🔗 Related Assignments
- **Assignment 4**: Functional Requirements → mapped to entities and rules
- **Assignment 6**: User Stories & Sprint Tasks → reflected in methods
- **Assignment 8**: Object State & Activity Diagrams → align with domain entities

---

## 📂 File Structure
```
/assignment9/
├── assignment9_domain_model.md   # Domain model, diagram, and reflection (this file)
└── README_assignment9.md         # Overview and traceability (you are here)
```

Let me know if you'd like a PDF version, image renders of the diagrams, or auto-linking to your GitHub repo!
