# Bridga Engineering: Consistency Check System

---

## **Objective**
Automate brand tone and style checks to ensure all content aligns with Bridga Engineering's established voice, tone, and messaging guidelines.

---

## **Steps to Set Up a Consistency Check System**

### **1. Define Tone and Style Preferences**
#### Tools Used: Grammarly Business, Writer
1. **Access Brand Settings**:
   - Log in to Grammarly Business or Writer.
   - Navigate to the **Style Guide** or **Tone Preferences** section.
   
2. **Set Key Preferences**:
   - **Tone**:
     - Professional
     - Confident
     - Approachable
   - **Style**:
     - Formal language for reports and emails.
     - Concise and clear wording for technical documents.
     - Conversational tone for social media and community outreach.

3. **Add Custom Brand Terminology**:
   - Define frequently used terms like "Sustainability," "Precision," and "Innovation."
   - Add common abbreviations or technical terms to avoid unnecessary corrections.

---

### **2. Review Existing Content for Consistency**
#### Tools Used: Grammarly Business, Writer
1. **Upload Documents**:
   - Gather existing brand assets, such as:
     - Website content
     - Marketing materials
     - Reports and presentations
   - Upload them into the **Content Review** section of Grammarly or Writer.

2. **Run Consistency Checks**:
   - Check for:
     - Adherence to tone and style preferences.
     - Consistent use of terminology.
     - Grammatical and punctuation errors.
     - Inconsistent formatting, such as headings or spacing.

3. **Generate Reports**:
   - Review flagged inconsistencies in the generated report.
   - Highlight areas requiring revision to align with brand guidelines.


---

# Automating Consistant Brand Tone and Style Check Setup Using Zapier

## **Objective**
Automate brand tone and style checks to ensure consistency across all content, streamline the review process, and reduce manual effort.

---

## **Workflow Steps**

### **1. Log into Zapier**
- Go to [Zapier](https://zapier.com) and log in or create a free account.
- Click on **"Create Zap"** to start building your automation.



![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(1).png)

---

### **2. Step 1: Trigger - New File in Google Drive**
- **App**: Google Drive
- **Event**: “New File in Folder”
  - Trigger the workflow when a new file is uploaded to a specific folder.
- **Setup**:
  - Connect your Google Drive account.
  - Specify the folder where files for review will be uploaded (e.g., "Content for Review").
- **Test**:
  - Upload a test file and verify that Zapier detects the trigger.




![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(2).png)


---

### **3. Step 2: Action - Upload Content for Review**
- **App**: Webhooks by Zapier (if no direct integration exists with Grammarly or Writer)
- **Event**: Custom Webhook Request
- **Setup**:
  - Use the API endpoint from Grammarly or Writer.
  - Send extracted text from the uploaded file (use Formatter by Zapier for text extraction if necessary).
- **Test**:
  - Confirm the file is successfully sent for analysis.



![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(3).png)



![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(4).png)



---

### **4. Step 3: Action - Create Task in Trello**
- **App**: Trello
- **Event**: “Create Card”
- **Setup**:
  - Board: “Content Review Workflow”
  - List: “Pending Review”
  - Add card details:
    - **Card Name**: File Name
    - **Description**: Include the Grammarly/Writer review link and deadline.
    - **Due Date**: Set it to 2 days after upload.
    - **Assignee**: Assign the task to a reviewer.
- **Test**:
  - Verify that a new card is created in the Trello board.



![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(7).png)


![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(6).png)



---

### **5. Step 4: Action - Notify Team on Slack**
- **App**: Slack
- **Event**: “Send Channel Message” or “Send Direct Message”
- **Setup**:
  - Notify the content reviewer or team about the new task.
  - Example Message:
    ```
    📄 New content ready for review!
    File Name: {{File Name}}
    Review Deadline: {{Due Date}}
    Trello Card: {{Trello Link}}
    ```
- **Test**:
  - Verify that notifications are sent correctly.



![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(5).png)


---

### **6. Step 5: Action - Update Trello Card After Review**
- **App**: Trello
- **Event**: “Update Card”
- **Setup**:
  - Move the card to the “Completed” list once the review is done.
  - Attach the Grammarly/Writer review report.
  - Add a checklist for flagged issues and required edits.
- **Test**:
  - Confirm that the card updates correctly.

---

### **7. Step 6: Action - Schedule Recurring Reviews**
- **App**: Google Calendar
- **Event**: “Create Event”
- **Setup**:
  - Create a recurring event for regular content reviews (e.g., weekly or monthly).
  - Title: “Monthly Brand Consistency Check”
  - Description: Include instructions for reviewing content.
- **Test**:
  - Verify the recurring event is added to Google Calendar.



![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(8).png)

---

### **8. Step 7: Action - Log Review Details in Google Sheets**
- **App**: Google Sheets
- **Event**: “Append Row”
- **Setup**:
  - Choose a spreadsheet (e.g., “Content Review Logs”).
  - Add columns for:
    - File Name
    - Reviewer Name
    - Review Completion Date
    - Flagged Issues
    - Resolutions Made
  - Log each review’s details in a new row.
- **Test**:
  - Ensure the data is appended correctly.



![Image Description](https://github.com/nikbearbrown/INFO-7375-Branding-and-AI/blob/main/Appendix/Module4/Images/Exercise4.2(9).png)

---

## **Optional Add-Ons**

### **1. Generate AI Summaries**
- **App**: OpenAI (ChatGPT)
- **Event**: “Summarize Content”
- **Setup**:
  - Send flagged issues to OpenAI for a concise summary.
  - Example:
    ```
    Summarize these flagged issues for content consistency.
    ```
- **Purpose**: Provide actionable insights for reviewers.

### **2. Automate Task Reminders**
- **App**: Slack or Email
- **Event**: “Send Reminder”
- **Setup**:
  - Notify reviewers if tasks remain incomplete by the due date.

---

### **3. Ensure Continuous Improvement**
1. **Collect Feedback**:
   - After every content review, collect feedback from editors and stakeholders to refine tone and style preferences.
   - Adjust settings in Grammarly/Writer based on feedback.

2. **Track Metrics**:
   - Monitor how often inconsistencies are flagged over time.
   - Aim for a reduction in flagged issues with each review cycle.

3. **Train Teams**:
   - Conduct training sessions for content creators on using Grammarly/Writer effectively.
   - Share best practices for adhering to Bridga’s tone and style.

---

## **Final Workflow Overview**
1. **Trigger**: New file uploaded to Google Drive.
2. **Review Submission**: File sent to Grammarly or Writer for tone and style checks.
3. **Task Creation**: Trello card created for tracking the review process.
4. **Team Notification**: Notify team members via Slack or email.
5. **Task Completion**: Update Trello card with review results.
6. **Recurring Reviews**: Automate monthly/weekly review schedules in Google Calendar.
7. **Data Logging**: Log review details in Google Sheets.

---

## **Expected Benefits**
- **Automation**: Reduces manual effort for tone and style checks.
- **Accountability**: Keeps team members informed and tasks on track.
- **Tracking**: Provides a clear history of content reviews and improvements.
- **Scalability**: Easily extendable for larger teams or additional content workflows.



---

