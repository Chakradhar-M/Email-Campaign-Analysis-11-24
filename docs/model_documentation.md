
###  Data Model Overview 

This data model consists of five tables designed to support a comprehensive analysis of email campaign performance. Below is a quick description of each table:

- **`email_data`**
- **`DateTable`**
- **`countries_data`**
- **`Measures_Table`**
- **`data_dictionary`**

### Table Relationships

| **Table**           | **Connected To** | **Type of Relationship** | **Join Column(s)**                   |
|---------------------|------------------|---------------------------|--------------------------------------|
| `DateTable`         | `email_data`     | One-to-Many               | `Date` → `Date_sent`                |
| `countries_data`    | `email_data`     | One-to-Many               | `country` → `country`               |
| `data_dictionary`   | None             | —                         | —                                    |
| `Measures_Table`    | None             | —                         | —                                    |

### Data Model Screenshot
![Data Model Screenshot](https://github.com/Chakradhar-M/Email-Campaign-Analysis-11-24/blob/main/resources/email_campaign_data_model.png?raw=true)
