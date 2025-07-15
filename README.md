# osTicket-Ticket-Lifecycle-Examples
*To explore the complete lifecycle of a support ticket using osTicket, in order to demonstrate understanding of ticket management and workflow in real IT enviornments.*

## Prerequisites
- [osTicket Installation within an Azure VM](https://github.com/EddieJIV/osticket-prereqs)
- [osTicket Post-Installation Configuration](https://github.com/EddieJIV/osTicket-Post-Installation-Configuration)

## Enviornments & Technologies Used

- Microsoft Azure (Virtual Machine)
- Remote Desktop
- Windows 10 OS
- Internet Information Services (IIS)
- osTicket

## Ticket Lifecycle Stages

**1. Ticket Creation:**

An end user submits a ticket about an issue (via portal, email, or call).

**2. Ticket Intake:**

The ticket is received and logged in the system. Initial default properties are set (priority, department, etc.).

**3. Ticket Categorization & Assignment:**

A help desk agent reviews the ticket, updates the category/help topic, sets urgency/severity, and assigns it to themselves, another agent, or a specific team/department.

**4. Initial Communication:**

The agent may contact the end user for clarification or more details.

**5. Ticket Work / Troubleshooting**

The agent investigates and attempts to resolve the issue, documenting actions and updates in the ticket.

**6. Escalation (if needed):**

If the issue is complex or out of scope, the agent escalates the ticket to a higher-level team or specialist.

**7. Resolution:**

Once the problem is fixed, the agent communicates the solution to the user and updates the ticket status to “Resolved.”

**8. Closure:**

The ticket is officially closed, completing the lifecycle.

---
#### Links for lab:
[Admin/Analyst Login Page](http://localhost/osTicket/scp/login.php) 

[End Users osTicket URL](http://localhost/osTicket) 

---
# Example 1: Entire mobile/online banking system is down

- First, we are going to create a ticket as Karen, the end-user we created in the last lab.

<img width="700" height="700" alt="End-User Portal" src="https://github.com/user-attachments/assets/2a92135c-f8ae-476d-89a9-350eaade0418" />


 - So, log into the end user portal using the link above.
 - Select, "Open a New Ticket"

<img width="700" height="700" alt="End-User Submission" src="https://github.com/user-attachments/assets/33b0345b-46d7-4836-995c-794bea2ab4f7" />



- Enter Karen's contact information.
- For the Help Topic, we are going to select **Report a Problem**

Keep in mind, we are going to enter this from the context/ point of view as the end-user (Karen) and not the IT Support specialist/ Agent to make it more realistic. 

Hence why we are simply selecting "Report a problem" rather than something more severe like "Report a problem/ Business Critical outage" because alot of the time the end-user will not necessarily put thje correct info into the ticket initially.

<img width="700" height="700" alt="Ticket Details- OBS" src="https://github.com/user-attachments/assets/f5bfe3b4-52cc-4870-bb95-490c3e680fc5" />

- Enter the above information into the Ticket Details from the perspective of Karen, then click create ticket.

<img width="700" height="700" alt="Agent Jane" src="https://github.com/user-attachments/assets/95fe35ea-69f9-4a5c-93a9-0903a9977375" />

- Once the Support ticket request is created, open up the osTicket agent panel in another tab/window, and log in as John, our supoport agent.

<img width="700" height="700" alt="Agent logged in" src="https://github.com/user-attachments/assets/c2661662-cc89-48b0-8d84-9066b67cd245" />

- First take note of the new open ticket that is now in the sytstem! You made that happen. All the way from creating the virtual machine on Azure that you're now working osTicket (that you installed and configured) in. Heck yeah!

- Click on the newly created ticket and lets observe the properties.

<img width="auto" height="auto" alt="Ticket 1 Properties" src="https://github.com/user-attachments/assets/58e4e593-185e-4703-9a60-8228934a4b4d" />

- Here we see that the priority of the ticket is normal, the department selected is the Support department, the ticket is not assisged to anyone in particular yet, and the default SLA plan is selected.
- But, based off of what we're reading, this appears to be a very serious ticket. As the help desk agent, we are going to adjust the ticket properties accordingly.
- In this case, as it seems very serious, we would most likely contact the person who made the ticket to speak with them on the phone/ or on teams to get a better understanding of the situation and its context.
- But, for this lab, we are just going to go ahead and set the properties of this ticket accordingly so it gets routed to the right place.

---

- First, click on the SLA plan.


<img width="700" height="700" alt="update SLA" src="https://github.com/user-attachments/assets/40a2a866-c548-42d7-afc0-154470bb9827" />


- For the SLA, since this is a very serious issue, we are going to set it to Sev-A.
  - As per las lab: Sev-A represents the highest priority level, typically reserved for critical issues that severely impact business operations or cause significant disruption.
  - Click update

<img width="700" height="700" alt="Update Help Topic" src="https://github.com/user-attachments/assets/62f40770-7892-4d04-9035-af1bcc368f2d" />

- Although the end-user was not necessarily wrong in putting "Report a Problem" for the help topic, what more appropriately would fit is Report a Problem / Business Critical Outage". Since the entire online baking system is down and no user can access it/ log in.
- Click update.

<img width="700" height="700" alt="Refresh Ticket- Thread" src="https://github.com/user-attachments/assets/95ff98d1-f500-4b87-84a1-bb19641f3c00" />

- If you refresh the ticket, youll notice that any changes we make to the ticket can be seen below in the ticket thread. This is beneficial for agents to see and observe ticket updates in real time and have an understanding on what part of the lifecycle this ticket is on and who is handling it/ working through it.

<img width="700" height="700" alt="Assign to a Team" src="https://github.com/user-attachments/assets/a54b3da6-bace-4b04-8acb-a284eede6a2e" />


- Finally, click on "Assigned To:"
- Naturally, we are going to assign this ticket to the Online Banking team as this explicitly has to do with Online Banking.
- Click Assign.
- Once we've updated the ticket properties we are going to log out of John's account.

<img width="700" height="700" alt="Jane login" src="https://github.com/user-attachments/assets/3c616d21-0220-460b-a135-8a7b3e0ada84" />

- Now that the ticket properties have been updated, and assigned to the right team, we are going to log in as our online banking team member Jane and "work" the ticket to completion. 








