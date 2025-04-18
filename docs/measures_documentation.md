

###  Measures Table Documentation

| **Measure Name**      | **Measure Function**                                               | **Measure DAX Formula**                                                                                                                                 |
|-----------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bounce Rate**        | Calculates the percentage of bounced emails in the total sent emails. | `Bounce Rate = DIVIDE(CALCULATE(COUNTROWS(email_data), email_data[bounced]=1), COUNTROWS(email_data), 0)`                                            |
| **Click Rate**         | Calculates the percentage of emails clicked by recipients.          | `Click Rate = DIVIDE(CALCULATE(COUNTROWS(email_data), email_data[clicked]=1), COUNTROWS(email_data), 0)`                                               |
| **Conversion Rate**    | Calculates the percentage of email recipients who converted.        | `Conversion Rate = DIVIDE(CALCULATE(COUNTROWS(email_data), email_data[conversion]=1), COUNTROWS(email_data), 0)`                                        |
| **Delivery Rate**      | Calculates the percentage of emails that were delivered (not bounced).| `Delivery Rate = DIVIDE([Emails Delivered], COUNTROWS(email_data), 0)`                                                                             
| **Open Rate**          | Calculates the percentage of emails opened by recipients.          | `Open Rate = DIVIDE(CALCULATE(COUNTROWS(email_data), email_data[opened]=1), COUNTROWS(email_data), 0)`                                                 |
| **Unsubscribe Rate**   | Calculates the percentage of unsubscribed emails.                   | `Unsubscribe Rate = DIVIDE(CALCULATE(COUNTROWS(email_data), email_data[unsubscribed]=1), COUNTROWS(email_data), 0) + 0`                             |
| **Emails Sent**        | Returns the total number of emails sent.                            | `Emails Sent = COUNTROWS(email_data)`                                                                                                                   |
| **Emails Delivered**   | Returns the total number of emails delivered (i.e., not bounced).  | `Emails Delivered = CALCULATE(COUNTROWS(email_data), email_data[bounced]=0)`                                                                         |
| **Opened Emails**      | Returns the total number of emails that were opened.               | `Opened Emails = CALCULATE(COUNTROWS(email_data), email_data[opened]=1)`                                                                               |
| **Unopened Emails**    | Returns the total number of emails that were not opened.           | `Unopened Emails = CALCULATE(COUNTROWS(email_data), email_data[opened]=0)`                                                                             |

