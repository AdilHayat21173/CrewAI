# Customer Support CrewAI Project  

This project demonstrates how to build an **AI-powered multi-agent support system** using the **CrewAI framework**.  
The system simulates a real-world **customer support process**, where different AI agents collaborate to provide complete, accurate, and friendly responses to customer inquiries.  

---

## 📌 Project Flow  

1. **Customer sends an inquiry**  
2. **Support Agent drafts a response**  
3. **Quality Assurance Agent reviews and refines the response**  
4. **Final polished response delivered to the customer**  

---

## 🧑‍💻 Components  

### 🔹 Agents  

Agents are like team members, each with their **role**, **goal**, and **backstory**.

| Agent | Role | Goal | Responsibilities |
|-------|------|------|------------------|
| **Support Agent** | Senior Support Representative | Provide friendly and helpful responses | Drafts complete answers, uses docs, ensures no assumptions |
| **QA Agent** | Support QA Specialist | Ensure top-quality support | Reviews drafts, ensures accuracy, improves tone and completeness |

---

### 🔹 Tools  

Tools extend the agents’ abilities.  

- **ScrapeWebsiteTool** → Allows agents to fetch information from CrewAI documentation.  
- Example: The Support Agent uses this tool to pull content from [CrewAI docs](https://docs.crewai.com/how-to/Creating-a-Crew-and-kick-it-off/).  

---

### 🔹 Tasks  

Tasks define **what each agent must do** and what the expected outputs are.  

| Task | Assigned Agent | Description | Expected Output |
|------|----------------|-------------|-----------------|
| **Inquiry Resolution** | Support Agent | Draft a response to the customer inquiry using all available info | A complete, detailed, and friendly draft response with references |
| **Quality Assurance Review** | QA Agent | Review and refine the Support Agent’s draft | A polished, customer-ready response with improvements |

---

### 🔹 Crew  

The **Crew** is the orchestrator that manages:  
- Which **agents** are included  
- Which **tasks** need to be completed  
- The **order of execution**  

In this project:  
- Task 1: **Inquiry Resolution** (Support Agent)  
- Task 2: **QA Review** (QA Agent)  
- Final Output: A **high-quality support response**  

---

## ⚙️ Execution Flow  

1. **Inputs provided to Crew**  
   - `customer`: The customer’s company (e.g., *AdilHayatAIDeveloper*)  
   - `person`: The contact person’s name (e.g., *Adil Hayat*)  
   - `inquiry`: The customer’s question (e.g., *“How can I add memory to my crew?”*)  

2. **Support Agent works first**  
   - Uses inquiry + tools (documentation)  
   - Prepares a detailed draft response  

3. **QA Agent reviews**  
   - Checks completeness and accuracy  
   - Refines tone and style  
   - Ensures no missing details  

4. **Final Answer Delivered**  
   - A polished, customer-ready response  

---

## 🌟 Key Highlights  

- 🤝 **Multi-Agent Collaboration** → Agents work like a real support team  
- 🛠️ **Tool Integration** → Agents use CrewAI documentation for accurate answers  
- 🔄 **Error Handling** → Retries if rate/token limits are reached  
- 🎭 **Realistic Backstories** → Agents act naturally thanks to detailed role context  

---

## 📖 Example Use Case  

- **Customer**: *AdilHayatAIDeveloper*  
- **Inquiry**: *“I need help with setting up a Crew and kicking it off, specifically how can I add memory to my crew?”*  

**Flow:**  
1. Support Agent → Drafts solution using docs  
2. QA Agent → Reviews and polishes the response  
3. Final Output → A **friendly, complete, and well-supported guide** for the customer  

---

## ✅ Conclusion  

This project is a **blueprint for AI-powered customer support** using CrewAI.  

It shows how:  
- **Agents with different roles** collaborate like a real support team  
- **Tasks and tools** structure their workflow  
- **Crew orchestration** ensures smooth execution  

 

---
