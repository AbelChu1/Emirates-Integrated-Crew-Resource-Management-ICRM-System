# Airline Crew Management System (ICRM)

## About This Project

In this project, we built a simplified airline crew management system that models how airlines handle crew scheduling, flight assignments, standby replacements, and final dispatch before flights.

The goal was not just to make the system work, but to implement everything using core data structures manually. We avoided using Python built-in structures like lists and dictionaries as the main storage, and instead focused on building everything from scratch.

This project is part of an ICS221 Data Structures and Algorithms course.

---

## What This System Does

We divided the system into four main parts, each representing a real operation in airline management:

- Managing crew flight schedules  
- Tracking all flights in the system  
- Handling standby crew replacements  
- Dispatching crew before departure  

Each part uses a different data structure depending on the problem we are solving.

---

## Data Structures Used

We used only the following:

- Singly Linked List  
- Doubly Linked List  
- Queue  

All structures were implemented manually using nodes and pointers.

---

## System Breakdown

---

### Phase I: Crew Roster (Singly Linked List)

We manage a crew member’s monthly schedule.

Flights are always kept in chronological order, even if they are added in the wrong order.

**We implemented:**
- Adding flights in sorted order  
- Removing flights using flight ID  
- Checking if there is at least 12 hours rest between flights  
- Displaying the full schedule  

**Why this structure?**  
A singly linked list allows us to insert flights in the correct position without shifting data.

---

### Phase II: Fleet Database (Doubly Linked List)

We store all flights and track how many crew members are assigned.

**We implemented:**
- Adding flights to the system  
- Updating crew count  
- Searching from both ends at the same time  
- Displaying staffing percentages  

**Why this structure?**  
We needed to search from both directions, which is only possible with a doubly linked list.

---

### Phase III: Standby Crew Pool (Queue)

We manage standby crew who can replace others in case of emergencies.

**We implemented:**
- Registering crew members  
- Finding a crew member with the required aircraft rating  
- Temporarily removing non-matching crew  
- Restoring the original order after the search  

**Why this structure?**  
A queue keeps the order fair and allows us to process crew one by one.

---

### Phase IV: Dispatch System (Modified Queue)

We manage crew dispatch before flights.

**We implemented:**
- Adding crew to the briefing system  
- Reordering based on departure time  
- Dispatching the crew with the earliest flight  
- Sending a confirmation message  

**Important detail:**  
Even though we used a queue, we modified insertion so that crew are ordered by departure time.

---

## Key Challenges

Some of the most difficult parts of this project were:

- Keeping data sorted without using built-in tools  
- Designing bidirectional search manually  
- Preserving order after temporarily removing elements  
- Handling real constraints like minimum rest time  
- Simulating priority behavior using basic structures  

---

## Complexity Considerations

We analyzed how each operation behaves:

- Most operations are linear time because we traverse linked structures  
- Queue operations like insertion and removal are constant time  
- Some operations require temporary structures, which increases space usage  

This helped us understand the trade-offs between simplicity and efficiency.

---

## What We Learned

This project helped us understand:

- How data structures actually work behind the scenes  
- Why choosing the right structure matters  
- How small design decisions affect performance  
- How to think step by step when solving problems  

It also improved our ability to write clean, structured, and well-documented code.

---

## Files Included

- `ICRM_System.ipynb` → Full implementation (Google Colab)  
- `ICRM_Report.pdf` → Detailed explanation and analysis  
- `README.md` → Project overview  

---

## Final Thoughts

This project shows how basic data structures can be used to model real-world systems. Even without advanced tools, we were able to build a working simulation by carefully designing each part.

It reinforced that understanding fundamentals is more important than relying on built-in shortcuts.
