## 3. Reflection 

### Challenges in Designing the Domain Model
One of the main challenges was selecting the appropriate **granularity** for both entities and attributes. Overcomplicating the model with excessive detail made it difficult to interpret and maintain, while too much abstraction risked omitting important behaviors and relationships. We found the best approach was to identify essential real-world objects (e.g., `UserAccount`, `Sensor`) and include only the attributes and methods most relevant to the system's functionality and user interactions.

### Mapping to Previous Assignments
Creating this model helped solidify connections between earlier work:
- **Assignment 4 (Functional Requirements):** Each entity directly reflects requirements (e.g., FR-005: "Issue weather alerts" aligns with the `Alert` entity).
- **Assignment 6 (User Stories & Sprints):** User interactions such as registering accounts, requesting forecasts, and managing locations directly map to methods and relationships.
- **Assignment 8 (Object Behavior & Workflows):** State diagrams created earlier now feel more grounded with clearer entity structures and transitions.

### Comparing Object Models with Activity Workflows
While activity diagrams (Assignment 8) focused on **processes and user/system behavior over time**, the class diagram focuses on **system structure and relationships**. Activity diagrams are excellent for modeling workflows, decisions, and roles, whereas class diagrams emphasize how data is organized and how entities interact structurally.

This dual perspective was essential: the class diagram provided architectural clarity, while activity diagrams highlighted procedural logic — and aligning both improved consistency across design documents.

### Lessons Learned
- Domain modeling should prioritize clarity and reusability.
- It is important to balance system-wide abstraction with object-specific details.
- Using Mermaid for class diagrams helped iterate quickly and stay aligned with previous artifacts.
- Modeling is most effective when supported by earlier agile documentation (requirements, user stories, state diagrams).

Overall, Assignment 9 provided valuable insight into connecting structural and behavioral modeling, and how both contribute to a scalable and maintainable software design.

