<h1 align="center">📧 Email Campaign Performance Analysis </h1>

<div style="display: flex; justify-content: space-between; padding: 10px; background-color: #f4f4f4; border-radius: 8px;">
  <h4>📅 Date: Nov 2024</h4>
  <h4>🛠️ Tools Used: Power BI, Excel, Figma</h4>
  <h4>🏷️ Domain: Marketing Analytics</h4>
</div>

---

### 📌 Background

Email marketing is one of the most powerful tools for digital platforms to stay connected with their audience, promote new offerings, and drive engagement. Especially for subscription-based content platforms, emails play a key role in announcing new features, encouraging participation in events, and converting readers into paying customers.

This project centers around a niche content platform that caters to a global community of DIY creators and readers. The platform regularly sends out email campaigns to inform users about product updates, online events, and subscription offers. These campaigns are crucial for building relationships with users and generating revenue.

To stay competitive and understand what works, the marketing team wants to track how these campaigns are performing across different audiences, regions, and device types. This involves looking into metrics like open rate, click rate, bounce rate, and conversion rate to make data-driven improvements.

---

### 🎯 Objective

To build a Power BI report that helps the marketing team:

✔️ Evaluate the performance of email campaigns from July to September 2024  
✔️ Identify which types of campaigns are most and least effective  
✔️ Analyze audience engagement by geography, device type, and email domain  
✔️ Understand what drives clicks, conversions, and unsubscribes  
✔️ Uncover opportunities to improve future campaign strategies

---

###  📂 Essential Project Links  

| 🧭 Resource | 🔗 Access |
|------------|----------|
| <img src="https://github.com/Chakradhar-M/PBI_Images/blob/main/Portfolio_Icons/database.png?raw=true" width="20" style="vertical-align:middle;"> **Data Source** | 👉 [Click to View Data Source](https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/challenges/fp20-analytics-october-2024) |
| <img src="https://github.com/Chakradhar-M/PBI_Images/blob/main/Portfolio_Icons/power-bi.png?raw=true" width="22" style="vertical-align:middle;"> **Power BI Live Report** | 📊 [View Interactive Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYmRkZTlkZTUtNTU2NC00MzViLWEyZWMtODRkNzcyYjNmYzk2IiwidCI6IjQ2NTRiNmYxLTBlNDctNDU3OS1hOGExLTAyZmU5ZDk0M2M3YiIsImMiOjl9) |
| <img src="https://github.com/Chakradhar-M/PBI_Images/blob/main/Portfolio_Icons/youtube.png?raw=true" width="20" style="vertical-align:middle;"> **Project Presentation** | 🎬 [Watch Presentation](#) |

📌 **Tip:** Right-click or Ctrl + Click to open links in a new tab.

---

### 📊 Sample Raw Data

<div style="overflow-x:auto;">

<table>
  <thead>
    <tr>
      <th>Campaign&nbsp;name</th>
      <th>Campaign&nbsp;type</th>
      <th>Conversion&nbsp;target</th>
      <th>Date&nbsp;sent</th>
      <th>client_email</th>
      <th>client&nbsp;segment</th>
      <th>country</th>
      <th>country&nbsp;latitude</th>
      <th>country&nbsp;longitude</th>
      <th>device</th>
      <th>clicked</th>
      <th>bounced</th>
      <th>opened</th>
      <th>unsubscribed</th>
      <th>conversion</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>After&nbsp;event&nbsp;follow&nbsp;up</td>
      <td>Events&nbsp;and&nbsp;webinars</td>
      <td>Download</td>
      <td>01-07-2024</td>
      <td>5zk9b92@gmail.com</td>
      <td>Lead</td>
      <td>India</td>
      <td>20.593684</td>
      <td>78.96288</td>
      <td></td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>After&nbsp;event&nbsp;follow&nbsp;up</td>
      <td>Events&nbsp;and&nbsp;webinars</td>
      <td>Download</td>
      <td>01-07-2024</td>
      <td>vh3xwzwkk3@yahoo.com</td>
      <td>Customer</td>
      <td>Afghanistan</td>
      <td>33.93911</td>
      <td>67.709953</td>
      <td></td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>After&nbsp;event&nbsp;follow&nbsp;up</td>
      <td>Events&nbsp;and&nbsp;webinars</td>
      <td>Download</td>
      <td>01-07-2024</td>
      <td>5s00qu@yahoo.com</td>
      <td>Customer</td>
      <td>Argentina</td>
      <td>-38.416097</td>
      <td>-63.616672</td>
      <td></td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>

</div>

🔗 Check out the **Data Dictionary** here 👉 [Click Here](https://github.com/Chakradhar-M/Email-Campaign-Analysis-11-24/blob/main/dataset/data_dictionary.md)

---


### 📊 **Key Performance Indicators (KPIs)**

1️⃣ **Bounce Rate**  
Represents the percentage of emails that were not successfully delivered (i.e., bounced). This metric helps evaluate the effectiveness of email delivery and the quality of the email list.

2️⃣ **Click Rate**  
Indicates the percentage of recipients who clicked on links within the email. This helps in understanding the level of engagement with the email content and its relevance to the audience.

3️⃣ **Conversion Rate**  
Measures the percentage of recipients who took a desired action (conversion) after receiving the email. This metric helps assess the success of the campaign in driving specific actions (such as purchases or sign-ups).

4️⃣ **Delivery Rate**  
Shows the percentage of emails that were successfully delivered to the recipient’s inbox, excluding bounced emails. This helps evaluate the overall success of email delivery.

5️⃣ **Open Rate**  
Represents the percentage of recipients who opened the email. It helps measure the effectiveness of the subject line and the level of interest generated by the email campaign.

6️⃣ **Unsubscribe Rate**  
Indicates the percentage of recipients who unsubscribed from the email list after receiving the campaign. A higher rate may signal dissatisfaction or over-frequency of emails.

7️⃣ **Emails Sent**  
Represents the total number of emails sent in the campaign. This helps track the volume of outreach and serves as a base for calculating other KPIs.

8️⃣ **Emails Delivered**  
Indicates the total number of emails successfully delivered to the recipients’ inbox. This helps gauge the accuracy and success of the email list and delivery strategy.

9️⃣ **Opened Emails**  
Shows the total number of emails that were opened by recipients. This metric is used to evaluate how compelling the email subject and content are in attracting attention.

🔟 **Unopened Emails**  
Represents the total number of emails that were sent but not opened by the recipients. This helps identify potential issues with email engagement and content appeal.



---
