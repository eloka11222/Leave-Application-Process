# Leave-Application-Process
A power automate project

## Introduction
![](https://github.com/eloka11222/Leave-Application-Process/blob/main/entire%20Process.jpg)

This Project stemmed from the need to automate basic rule-based processes using power automate. The entire process is quite simple. The User fills a leave request form created using Microsoft Forms. Then he submits the form, the process is triggered. An approval request gets sent to his manager. If the manager approves the leave, the HR receives the leave request showing that it has been approved by the manager. If the HR approves the leave request, the respondent gets notified via email and the form details are stored in the Approved Worksheet of the Leave applications Workbook which is stored in in OneDrive. If either the HR or the manager denies the request, then the respondent gets notified that his leave application has been denied along with where it was denied. 

## Connectors Used
![](https://github.com/eloka11222/Leave-Application-Process/blob/main/connectors%20used.jpg)

- Microsoft Forms Connection : Connection Helps me get the response ID, together with the response details
  ![](https://github.com/eloka11222/Leave-Application-Process/blob/main/Form.jpg)
  
- Office 365 Users Connection: This connection helps me get the manager of the respondent using the User Principal Name (login email address) which is tied his manager.
- Approvals Connection: this connection helps me create approval requests. 
- Office 365 Outlook Connection: this connection helps me send emails to the respondents
- Excel Online (Business) Connection: this connection helps me write files directly to the Excel file stored in the OneDrive folder.

  ## Process Explanatioon

  ### Trigger

  When a new Response is submitted (Microsoft Forms Connection)
 ![](https://github.com/eloka11222/Leave-Application-Process/blob/main/trigger.jpg)

  ### Actions

- Get Response details from the response ID (Microsoft forms Connection)
![](https://github.com/eloka11222/Leave-Application-Process/blob/main/Get%20Response.jpg)

- Get Manager (using the Microsoft Office 365 Users Connection)
![](https://github.com/eloka11222/Leave-Application-Process/blob/main/Get%20manager.jpg)

- Start and Wait for Approval (Approvals Connection)
![](https://github.com/eloka11222/Leave-Application-Process/blob/main/Manager%20approval.jpg)

Conditions: since the approvals will either come back as approved or denied, the condition catches both scenarios and branches off to other processes for each scenario
![](https://github.com/eloka11222/Leave-Application-Process/blob/main/Condition.jpg)

## Conclusion

Although this was quite a simple automation. it's importance cannot be undervalued. i hoope this process meets business requirements. Please reach out to me if you feel i missed steps or got the process wrong

