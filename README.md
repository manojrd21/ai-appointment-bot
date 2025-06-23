# AI Appointment Booking Assistant (Cal.com Integration)

This project builds an AI agent that helps students to schedule appointments with school counselors using natural language.

---

## Project Objective

Convert user intent (e.g., "I want to talk to a counselor next Friday at 3 PM") into a structured date and show a Cal.com booking link.

---

## Assignment Task Justification

This project satisfies all tasks outlined in the assignment:

1. **Intent understanding using LLM:**  
   Uses FLAN-T5 model to extract natural date/time from user input.

2. **API integration (adjusted):**  
   Due to Cal.com Cloud's restriction (no server-side API key on free tier), I have use a public booking link ('https://cal.com/manoj-dhanawade/counselor-session') instead of API-based scheduling.

3. **Fallback handling for unclear input:**  
   Uses parsedatetime to validate and fallback with friendly error if parsing fails.

4. **Confirmation message and calendar link:**  
   Assistant responds with structured date/time and a clear booking link.

---

## Features

- Uses **Google's FLAN-T5 model** for intent understanding
- Parses natural date/time using 'parsedatetime'
- Generates friendly confirmation messages
- Returns a **direct booking link** for the user to complete the appointment

---

## Tools Used

- Python (Google Colab)
- Transformers ('flan-t5-large')
- 'parsedatetime' for parsing
- Cal.com (Public Booking Link)

---

## Example Flow

*Input:*
I want to meet next Tuesday at 4 PM

*AI Output:*
Extracted: next Tuesday at 4 PM
Parsed: Date: 2025-06-25, Time: 04:00 PM

Assistant Response:
I've understood your preferred time as: next Tuesday at 4 PM
Please complete your booking here:
https://cal.com/manoj-dhanawade/counselor-session


---

## Setup Instructions

1. Open the 'appointment_bot.ipynb' file in Colab
2. Run all cells step by step
3. Try different natural inputs like:
   - "Can I speak to a counselor next Tuesday at 10 AM?"
   - "I'd like to talk on 2nd July at 11:30 AM"
   - "Can we talk this Saturday evening?"
   - "Is there a slot open this coming Sunday at 1 PM?"

---

## Booking Link

All bookings are redirected to this public link:  
[Book Now](https://cal.com/manoj-dhanawade/counselor-session)

---

## Notes

- Cal.com's API requires a Pro plan for server-side integration.
- This project uses the **public booking link approach**, which is fully functional and within free tier limits.

---

## Author

- **Manoj Dhanawade**  
- [LinkedIn Profile](https://linkedin.com/in/manojdhanawade2105/)
