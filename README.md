Khristin Schenk
February 9, 2025
SDEV220, Fall 2025

# Module 3: Final Project Launch
[Link to Trello Board](https://trello.com/invite/b/67b7abfc18f18ce15b085bfb/ATTI33b20571a5d8fcfcf77f75b7131772531A707EB3/sdev-220)

### Python Application for: *Bath & Body Works*

**Overview**  
This Python application is designed for Bath & Body Works customers to log and track their favorite fragrances by year and season. Users can create shopping lists linked to birthdays, holidays, and special occasions, organizing purchases by week, day, and year.

**Key Features**  
- **Fragrance Collection Management:** Users can add fragrances to a personal inventory.
  
- **Seasonal Organization:** Fragrances can be categorized by year and season.
  
- **Shopping List Integration:** Users can create lists for birthdays, holidays, and special events.
  
- **Status Labels:** Assign statuses such as “SHOPPING LIST,” “I Have Not Smelled,” “I Like This One,” etc.
  
- **Data Storage & Retrieval:** Save and access lists using a JSON file.
  
- **Data Organization:** Organized by Year & Month.  

- **Shopping List & Status Options:** Saved lists and statuses may include:  
  - **Shopping Lists:** Drafts, Final, Last Year, This Year, All Time  
  - **Status Options:** Create Shopping List, Import Shopping List, Save/Edit, Update, Birthday History by Year 

- **User Prompts & Actions:**  
  - Create and manage lists.  
  - Create a shopping list.  
  - Open an existing list (Dropdown menu for available years).  
  - Edit, export, or share lists.  
  - Enable notifications via phone or email.  

- **Updating Information:**  
  - Confirm updates before exiting.  
  - Prompt users to save changes.  

- **Birthday Computation Feature:**  
  To calculate ages within the program, the following formulas can be used:  
  ```csv
  - Years: `=DATEDIF(A1, TODAY(), “Y”)`  
  - Months Since Last Birthday: `=DATEDIF(A1, TODAY(), “YM”)`  
  - Days Until Next Birthday: `=DATEDIF(A1, TODAY(), “MD”)`  
  - Formatted Output: `=CONCAT(A2, " years, ", A3, " months, ", A4, " days ")`
  ```  
 
  **To-Do:** Implement an Excel file that includes these formulas for birthday tracking.

- **Data Fields:**  
  - Year & Month – Organized by year, with individual months listed.  
  - Day (01-31) – Assign specific events or purchases to each day.  
  - Name Format – (Last, First) or (First, Last).  
  - Age This Year – Automatically calculated and displayed.  

- **User Editing Options:**  
  - Create a shopping list.  
  - Edit an existing list.  
  - Export/share lists.  
  - Set push/email reminders.  
  - Project Inspiration.
