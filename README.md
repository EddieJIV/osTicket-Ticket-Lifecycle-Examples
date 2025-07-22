<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket-Ticket-Lifecycle-Examples
*To explore the complete lifecycle of a support ticket using osTicket, in order to demonstrate understanding of ticket management and workflow in real IT environments.*

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
 - Select, "Open a New Ticket".

<img width="700" height="700" alt="End-User Submission" src="https://github.com/user-attachments/assets/33b0345b-46d7-4836-995c-794bea2ab4f7" />



- Enter Karen's contact information.
- For the Help Topic, we are going to select **Report a Problem**.

Keep in mind, we are going to enter this from the context/ point of view as the end-user (Karen) and not the IT Support specialist/ Agent to make it more realistic. 

Hence why we are simply selecting "Report a problem" rather than something more severe like "Report a problem/ Business Critical outage" because a lot of the time the end-user will not necessarily put the correct info into the ticket initially.

<img width="700" height="700" alt="Ticket Details- OBS" src="https://github.com/user-attachments/assets/f5bfe3b4-52cc-4870-bb95-490c3e680fc5" />

- Enter the above information into the Ticket Details from the perspective of Karen, then click create ticket.

<img width="700" height="700" alt="Agent Jane" src="https://github.com/user-attachments/assets/95fe35ea-69f9-4a5c-93a9-0903a9977375" />

- Once the Support ticket request is created, open up the osTicket agent panel in another tab/window, and log in as John, our support agent.

<img width="700" height="700" alt="Agent logged in" src="https://github.com/user-attachments/assets/c2661662-cc89-48b0-8d84-9066b67cd245" />

- First, take note of the new open ticket that is now in the system! You made that happen. All the way from creating the virtual machine on Azure that you're now working on osTicket (that you installed and configured) in. Heck yeah!

- Click on the newly created ticket and let's observe the properties.

<img width="auto" height="auto" alt="Ticket 1 Properties" src="https://github.com/user-attachments/assets/58e4e593-185e-4703-9a60-8228934a4b4d" />

- Here we see that the priority of the ticket is normal, the department selected is the Support department, the ticket is not assigned to anyone in particular yet, and the default SLA plan is selected.
- But, based on what we're reading, this appears to be a very serious ticket. As the help desk agent, we are going to adjust the ticket properties accordingly.
- In this case, as it seems very serious, we would most likely contact the person who made the ticket to speak with them on the phone/ or on Teams to get a better understanding of the situation and its context.
- But, for this lab, we are just going to go ahead and set the properties of this ticket accordingly so it gets routed to the right place.

---

<img width="700" height="700" alt="update SLA" src="https://github.com/user-attachments/assets/40a2a866-c548-42d7-afc0-154470bb9827" />

- First, click on the SLA plan.
- For the SLA, since this is a very serious issue, we are going to set it to Sev-A.
  - As per the last lab: Sev-A represents the highest priority level, typically reserved for critical issues that severely impact business operations or cause significant disruption.
  - Click update

<img width="700" height="700" alt="Update Help Topic" src="https://github.com/user-attachments/assets/62f40770-7892-4d04-9035-af1bcc368f2d" />

- Click on the help topic to update it.
- Although the end-user was not necessarily wrong in putting "Report a Problem" for the help topic, what more appropriately would fit is Report a Problem / Business Critical Outage". Since the entire online baking system is down and no user can access it/ log in.
- Click update.

<img width="700" height="700" alt="Priority level" src="https://github.com/user-attachments/assets/1e9f7f7f-6897-418f-8d60-094552c1d56c" />

- In that same vein, we are going to set the priority level to emergency.


<img width="700" height="700" alt="Refresh Ticket- Thread" src="https://github.com/user-attachments/assets/95ff98d1-f500-4b87-84a1-bb19641f3c00" />

- If you refresh the ticket, you'll notice that any changes we make to the ticket can be seen below in the ticket thread. This is beneficial for agents to see and observe ticket updates in real time and have an understanding on what part of the lifecycle this ticket is on and who is handling it/ working through it.

<img width="700" height="700" alt="Assign to a Team" src="https://github.com/user-attachments/assets/a54b3da6-bace-4b04-8acb-a284eede6a2e" />


- Finally, click on "Assigned To:"
- Naturally, we are going to assign this ticket to the Online Banking team as this explicitly has to do with Online Banking.
- Click Assign.
- Once we've updated the ticket properties, we are going to log out of John's account and move on to the next stage of the ticket's lifecycle.

<img width="700" height="700" alt="Jane login" src="https://github.com/user-attachments/assets/3c616d21-0220-460b-a135-8a7b3e0ada84" />

- Now that the ticket properties have been updated and assigned to the right team, we are going to log in as our online banking team member Jane and "work" the ticket to completion.
- Once logging in, click on the ticket to get back into the ticket details.

<img width="700" height="700" alt="Jane takes ticket" src="https://github.com/user-attachments/assets/2ab23d5b-c327-4209-8857-6c4decfb1635" />

- Notice how this ticket is effectively assigned to the entire online baking team currently.
- As Jane, we are going to take this ticket over and act as if she will be the one to theoretically work the ticket to completion.

<img width="700" height="700" alt="Update assignee" src="https://github.com/user-attachments/assets/86a449ee-f895-4d7f-9ea1-9964984cee8a" />

- Click on who it is assigned to and we will update the Assignee to Jane.

<img width="700" height="700" alt="Assignee updated to OB/Jane" src="https://github.com/user-attachments/assets/ac135ffb-1683-42ce-83d9-2dd2ed2fa2fb" />
 
- Notice how the Assigned to section is now labeled as Jane Doe/Online banking.

<img width="700" height="700" alt="client update" src="https://github.com/user-attachments/assets/765f5c41-d89f-467b-ae74-e3758acb1088" />

- Now, we are going to update the client about her ticket to keep her in the loop about what we are doing to work her ticket to completion.
- Click Post Reply.

<img width="700" height="700" alt="Rollback" src="https://github.com/user-attachments/assets/b0e463c8-94c0-4968-bffc-4ed2b1d49270" />

- Next, let's update the client and inform her that we were able to determine a cause for the issue, that a resolution has been put into place, and that Online Banking should be up and running again.
- Click post reply.

<img width="700" height="700" alt="Work trail" src="https://github.com/user-attachments/assets/16b779b1-998f-4a00-8031-0315d2d4eadb" />

- Notice how osTicket shows us the "trail" of work that has been done to get this ticket from its opening stages to its resolution.

<img width="700" height="700" alt="700" src="https://github.com/user-attachments/assets/d2adb80a-b1d5-465a-b29d-a6cc3847b8fa" />

- Now that the issue has been fixed and the end user has been updated, let's close out the ticket.
- We can now update the status of the ticket to resolved, simply by clicking on its current status, marking it resolved, and clicking close!

 <img width="700" height="700" alt="resolved" src="https://github.com/user-attachments/assets/3de6b423-76e1-43fd-abc2-9dd2c25b87b3" />

Congratulations! We've meticulously navigated the lifecycle of a help desk ticket, starting from its creation by end-user Karen, to its successful resolution by agent Jane, and successfully resolved a Help Desk ticket within osTicket! 

Now, on to the next example:

# Example 2: "Adobe Broke"

<img width="700" height="700" alt="Example 2" src="https://github.com/user-attachments/assets/fd7ed77a-60c5-4110-95bd-77a9de512b78" />

- Utilize the end user portal to open a new Ticket as our end-user Karen.

<img width="700" height="700" alt="image" src="https://github.com/user-attachments/assets/5364b5f3-a8fc-45ea-8a51-8e799173676b" />

- Enter the information above into the the new ticket's details. Click Create Ticket.
- Notice how this ticket is also very ambiguous and is made out to seem almost like a critical outage.
  - *It should be quickly determined that reaching out to the customer who submitted the ticket to gain a better understanding of the context of the situation would be very helpful.*
 
 <img width="700" height="700" alt="John login" src="https://github.com/user-attachments/assets/2ac74c1e-43e3-4dcb-8614-ee9477098b1f" />

 - Log back in as John for further investigation of the issue.

 <img width="700" height="700" alt="Initial Ticket inspection" src="https://github.com/user-attachments/assets/51c24913-65b0-44a6-9412-5a66cefe0e48" />


- We can see that the ticket from Karen has come through, and we are going to analyze the issue for a more detailed categorization and further assignment of the ticket.
- Again, a good place to start with this after initially analyzing the ticket and noticing that it is very ambiguous would be to contact Karen and essentially ask her what she exactly means by "many people can't use their Adobe accounts".
- From our conversation with Karen, it's determined that "Many people" turned out to be Karen and one other person, and that the Adobe software on their computer simply will not open/run.
- After hearing this, you politely ask Karen if she can restart her computer and try to re-open Adobe. She says to you that her and her department are about to go on lunch and will try when she returns.
- In the meantime, we can now update our ticket properly with the actual context of the situation at hand.

<img width="700" height="700" alt="overview" src="https://github.com/user-attachments/assets/59d25133-5d38-4b49-941a-8e9679803b82" />

- With our now detailed understanding of the ticket, it looks like the priority, Help Topic, and Department are all categorized sufficiently.
- We simply need to take the ticket over as John, and assign a proper SLA.

<img width="700" height="7009" alt="Assignee" src="https://github.com/user-attachments/assets/001aa9d6-73b3-47f0-8aa9-16d77fd6a4f2" />

- Click on Assign to and take the ticket over as John.

<img width="700" height="700" alt="Update SLA" src="https://github.com/user-attachments/assets/f28db769-6002-46bb-b611-dd5c4a136f7a" />

- Next, click on SLA Plan.
- Since we know it's only two people in the department having this issue and not the whole department, we can set the Sev to Sev-C.

<img width="700" height="700" alt="Log update" src="https://github.com/user-attachments/assets/d4ed2bb5-4250-4bc5-ba57-7b2896ab0206" />

- Now, let's update the ticket notes. It is important to know that this is how not only the IT department, but the customer as well, will be updated on the progress of the ticket. Click Post reply.

---
~ Lunchtime passes ~

---

- Karen calls back and she says that they restarted their computers, and their Adobe Readers are working just fine, and there are no more issues. Great!

<img width="700" height="700" alt="Resolved note" src="https://github.com/user-attachments/assets/5dd6e298-dfef-474c-af98-9a1cb97f8642" />

- Now we can make another note in the ticket explaining the call we just had with Karen, and noting that the ticket will subsequently be closed.

<img width="700" height="700" alt="RESOLVED" src="https://github.com/user-attachments/assets/819e21fc-27c7-4aa0-b147-fe62383af7d1" />

- Now that the ticket's notes log has been updated with everything we have done from initial intake, all the way to the resolution of the ticket, we can go ahead and set the status of this ticket to resolved! 

<img width="700" height="700" alt="No Open tickeys" src="https://github.com/user-attachments/assets/fd0caa1d-833d-4d2e-8b57-a75c77ab5b3d" />

- After hitting close, you should be routed back to the ticket dashboard and see that there are no more open tickets.

<img width="700" height="700" alt="Closed tickets thus far" src="https://github.com/user-attachments/assets/f3e87bba-dac8-42b0-be32-82aed843e32a" />


- By navigating to the Closed tab under the Tickets heading, you should be able to see the ticket we just worked to completion as well as the first one.

Congratulations! That's another ticket down. We successfully navigated the ticketing process for a reported issue with Adobe, transforming an ambiguous ticket into a clear and actionable support request. By engaging with the end-user, Karen, we clarified the situation, categorized the ticket appropriately, and assigned the correct SLA. After troubleshooting and confirming the resolution, we documented each step, ensuring transparency and effective communication. 

# Example 3: CFO's Laptop won't turn on

- For this example, we are going to pretend like the CFO personally called you in a frenzy because he has a meeting with the company's board members in 30 minutes and their laptop will not turn on.
- With this information, you understand that time is of the essence so you kindly and calmly ask them for permission to swing by their office to take a look at it.

<img width="700" height="700" alt="Adminuser login" src="https://github.com/user-attachments/assets/b3f9086e-b0ba-4743-bf11-8fcc044d5ca3" />

- Sign into your (adminuser) osTicket account. 
- With the understanding that this is a bit of an emergency for the CFO you do not bother to ask them to submit a ticket, knowing you can quickly do it yourself prior to heading over to the CFO's office.

<img width="700" height="700" alt="New Ticket" src="https://github.com/user-attachments/assets/0730a7bc-b4d6-428e-82de-9abba61ba117" />

- Open up the Agent Panel and navigate to Tickets > New Ticket
  - Click on New Ticket

<img width="700" height="700" alt="Add CFO" src="https://github.com/user-attachments/assets/cc4a8286-d9d9-4d58-aa50-cab493dc4028" />

- For the sake of this lab, we are going to quickly add an account for the CFO.
  - Obviously, if this were a real-life scenario, the CFO would have an account that we would select at this point. So we can just use this as practice with navigating the software and building intuition!
- Click Add User.

<img width="700" height="700" alt="Initial details" src="https://github.com/user-attachments/assets/fdd74855-588c-495b-91cd-cdd94f471503" />

- Begin filling out the initial ticket details.
- Since the CFO called us, we are going to make the ticket source the phone, set the alert to alert user, and at this point, we can use our intuition to fill out the Help Topic and Department.
- Since the context of the situation is that their laptop is not working and is needed for a meeting with the company's board members in 30 minutes, we are going to mark it as Sev-A.
- Assign it to yourself. You'll be taking this one!
- Fill out the rest of the details as seen above.

<img width="700" height="700" alt="initial response" src="https://github.com/user-attachments/assets/1b743a62-6ba7-4dc0-89fc-35252c29f2df" />

- Moving down the line, we are going to set the priority to high as this ticket needs to be resolved within the next 20-25 minutes or they will miss their board meeting.
- We will also provide our initial response to the situation, then click on Open.

<img width="700" height="700" alt="new ticket" src="https://github.com/user-attachments/assets/967c2d19-ab8e-4ffe-a1e5-d28a26363183" />

- Here we can see our newly created ticket and quickly scan over it to make sure everything looks correct, then we will hop into action.

<img width="700" height="700" alt="broken charger" src="https://github.com/user-attachments/assets/bce44683-56d4-4ed6-8cf5-828f4df77258" />

- In this case, it turns out that the issue was just a broken charger thankfully and not a more technical hardware issue. We quickly replace the charger for the CFO, notice the laptop boots up just fine now and we head back to our desk to close the ticket!
- First, we need to update the notes for the ticket, explaining what we did to resolve the issue.
- Click post reply.

<img width="700" height="700" alt="image" src="https://github.com/user-attachments/assets/8f47adad-2514-456d-ad6b-4c30b798fce4" />


- Click on the ticket's status that is currently set to open, and change it to resolved!
- Briefly explain the issue and how it was resolved, then hit close! Crisis averted!!!



## Conclusion
This concludes our final project in the osTicket lab series!!! In this lab we have successfully navigated through the lifecycle of three distinct help desk tickets, demonstrating a fundamental understanding of ticket management and workflow in real IT environments.

This hands-on experience with osTicket not only reinforced our technical knowledge, but also prepared us for real-world scenarios in IT support. Obviously, there is much more to this product that covered here. Thus, I recommend taking the time to play around in osTicket by creating and working different tickets. Use your imagination and have fun being your own Help Desk.


If you made it this far, I want to take a moment to sincerely thank you for joining me on this journey. It’s been a long road, and your dedication and enthusiasm have made it all the more rewarding. 

Thank you for being a part of this experience!


















