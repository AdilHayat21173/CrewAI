# EventAutomation CrewAI Project

This project demonstrates how to automate event planning and management using the CrewAI multi-agent framework. The system simulates a real-world event management team, where specialized AI agents collaborate to handle venue selection, logistics, and marketing for an event.

---

## 🎯 Main Purpose

**EventAutomation** is designed to:
- Automate the process of organizing events (seminars, conferences, etc.)
- Assign specialized AI agents to handle different aspects of event management
- Use real-time web search and data extraction tools for accurate, up-to-date information
- Output structured results (venue details, logistics confirmation, marketing report) in ready-to-use formats

---

## 🤖 What Can This Project Do?

Imagine you want to book a hall for your seminar, but you don’t want to walk everywhere or call every venue. With this bot, you simply provide your event requirements (topic, city, date, budget, expected participants), and the system will:
- Search for available halls in your city that fit your budget and participant needs
- Scrape the web for up-to-date venue details (capacity, location, booking status)
- Suggest the best options and output all details in a structured file
- Coordinate logistics (catering, equipment) and confirm arrangements
- Plan and report on marketing activities to maximize attendance

**Example:**  
If you want to organize an "Agentic AI Seminar" in Peshawar for 200 people with a budget of $10,000, just enter these details. The bot will:
- Find suitable seminar halls in Peshawar
- Check if they are available and within your budget
- Provide you with all the details (address, capacity, booking status)
- Arrange catering and equipment for the event
- Generate a marketing plan and engagement report

You don’t need to visit venues or call providers—the bot does all the research and coordination for you!

---

## 🧑‍💻 Agents & Their Roles

| Agent Name                    | Role & Goal                                                                                   | Responsibilities                                                                                  |
|-------------------------------|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| **Venue Coordinator**         | Find and book the best venue for the event                                                   | Searches for venues, checks capacity/location, ensures suitability, outputs structured details     |
| **Logistics Manager**         | Manage all event logistics                                                                  | Arranges catering, equipment, and other logistics, confirms all arrangements                      |
| **Marketing & Communications**| Promote the event and engage participants                                                    | Crafts marketing messages, communicates with attendees, reports on engagement                     |

---

## 🛠️ Tools Used

- **SerperDevTool**: For web search (venue info, logistics providers, etc.)
- **ScrapeWebsiteTool**: For extracting details from specific web pages

---

## 🚦 Step-by-Step Workflow

1. **Set Up Environment**
   - Add your API keys and model name to the `.env` file:
     ```
     GROQ_API_KEY=your_groq_api_key
     GROQ_MODEL=your_model_name
     SERPER_API_KEY=your_serper_api_key
     ```

2. **Define Event Details**
   - Specify the event topic, city, date, expected participants, and budget in the code.

3. **Initialize Agents**
   - Each agent is created with a clear role, goal, backstory, and access to the necessary tools.

4. **Define Tasks**
   - Each task is assigned to the appropriate agent:
     - **Venue Selection**: Find and book a suitable venue.
     - **Logistics Coordination**: Arrange catering and equipment.
     - **Marketing**: Promote the event and engage attendees.

5. **Create the Crew**
   - All agents and tasks are grouped into a CrewAI `Crew` object.

6. **Run the Workflow**
   - The crew is kicked off with the event details as input.
   - Agents collaborate to complete their tasks in sequence.

7. **Output Results**
   - Venue details are saved as `venue_details.json`.
   - Marketing report is saved as `marketing_report.md`.
   - Logistics confirmation is printed to the console.

8. **Review Outputs**
   - Open `venue_details.json` for venue info.
   - Open `marketing_report.md` for the marketing summary.

---

## ▶️ How to Run

1. Install dependencies:
    ```bash
    pip install crewai[tools] python-dotenv
    ```

2. Set up your `.env` file as described above.

3. Run the notebook `main.ipynb` in the `EventAutomation` folder.

---

## 📋 Example Event Details

```python
event_details = {
    'event_topic': "Agentic AI Seminar",
    'event_description': "A seminar bringing together AI enthusiasts, students, and professionals to discuss the future of Agentic AI and its applications.",
    'event_city': "Peshawar",
    'tentative_date': "2025-08-30",
    'expected_participants': 200,
    'budget': 100000,
    'venue_type': "Seminar Hall"
}
```

---

## 💡 Key Features

- **Multi-Agent Collaboration**: Each agent specializes in a core event management function.
- **Real-Time Data**: Uses web search and scraping for up-to-date information.
- **Structured Outputs**: Venue and marketing details are saved in files for easy access.
- **Error Handling**: Automatic retries for rate/token limit errors.
- **No More Manual Searching**: The bot finds the best venues and solutions for you, saving time and effort.

---

## 📚 Learn More

- [CrewAI Documentation](https://docs.crewai.com/)
- [Groq API Documentation](https://console.groq.com/docs)

---

## 📝 License

This project is for educational and development purposes. Please ensure compliance with CrewAI and Groq