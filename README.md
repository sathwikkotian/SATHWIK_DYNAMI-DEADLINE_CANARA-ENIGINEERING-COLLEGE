# SATHWIK_DYNAMI-DEADLINE_CANARA-ENIGINEERING-COLLEGE
This project automates task management in Asana by assigning due dates based on task priority and extending due dates for tasks in the "In Progress" section. It uses the Asana API to update task details, ensuring real-time alignment of deadlines for high-priority tasks.

Key Features:
Dynamic Due Dates:

Low Priority: Due date = 14 days from today.
Mid Priority: Due date = 7 days from today.
High Priority: Due date = 2 days from today.
In Progress Section Automation:

When a task is moved to "In Progress" and has High priority, all tasks in the "In Progress" section will automatically have their due dates extended by 2 days.
Avoid Redundant Extensions:

The system ensures that the due date extension happens only once per status change event.
------------------------------------------------------------------------------------------------------------------------------------------------------------
Prerequisites
Before running this project, ensure you have the following:

Python 3.x installed.
Asana Personal Access Token (API credentials).
Required libraries: requests, json.
----------------------------------------------------------------------------------------------------------------------------------------------------------
Follow these steps to set up the project on your machine or in a Google Colab environment.

Clone the Repository: Clone the repository to your local machine or Google Colab
git clone https://github.com/sathwikkotian/SATHWIK_DYNAMI-DEADLINE_CANARA-ENIGINEERING-COLLEGE.git



Install Dependencies: Install the required Python libraries.
pip install requests
Set up Asana API:

Get your Asana Personal Access Token from Asana's Developer page.
Store your token in a safe place and use it in the script for API access.




Usage
To run the script and automate the task process, follow these steps:

Open the Python script (asana_task_automation.py or similar) in your editor.

Authenticate with Asana API:

Update the API_KEY in the script with your Asana personal access token.
Run the Script: Execute the script in your terminal or environment:


python asana_task_automation.py


Example Input
You can provide a task's details in JSON format as follows to test the automation:

{
  "task_id": "1234567890",
  "priority": "High"
}


This input will:

Set the task's due date to 2 days from today.
Update all tasks in the "In Progress" section (if the priority is High) by extending their due dates by 2 days.

Example Output:
The task with ID 1234567890 will have its due date updated automatically based on its priority, and all tasks in "In Progress" with high priority will be extended by 2 days.
