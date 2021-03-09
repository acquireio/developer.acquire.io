# Overview

The Acquire Analytics provides you with the necessary resources to gain a deeper understanding of your agent and customer behavior on your system. This API allows you to export your data, based on a standard format, from which you can implement your system and any other system that you can use to manage your data.

### **Mandatory parameters**

These parameters are mandatory in all analytics APIs.

| Name | Type | Description |
| :--- | :--- | :--- |
| start\_date | datetime | Date from \(format: YYYY-MM-DD, eg: 2020-01-16 or YYYY-MM-DD HH:MM:SS, e.g. 2020-01-16 00:00:00\) |
| end\_date | datetime | Date to \(format: YYYY-MM-DD, eg: 2020-10-16 or YYYY-MM-DD HH:MM:SS, e.g. 2020-10-16 23:59:59\) |
| offset | string | This parameter is used for the timezone value and the default timezone will be "GMT". e.g. +05:30 |

