# SAP Cloud Integration - Certificate Expiry Reminder Iflow
Ready to use! Upload to a package, configure it and deploy. 

This is a working and fully implemented version of this idea: SAP CPI Keystore Expiry – Email Notification – Simplest of All | SAP Blogs (https://blogs.sap.com/2023/05/17/sap-cpi-keystore-expiry-email-notification-simplest-of-all/). 

---

### Explanation/Installation: 
The mapping checks for each certificate if the configured alert threshold in days is reached. E.g. 60 days threshold means that the alert is sent if expiry is <60 days in the future. 
If no certificate is expiring, no email is sent (router added for this). 
The email body can be changed in the email channel. The subject is configurable.

To access the key store, you need to create a service key (or reuse an existing one) with plan "api" and an appropriate role to read the Key Store, e.g. AuthGroup_IntegrationDeveloper. Save it as OAuth credential in Security Materials, e.g. with name BTP_API_OAUTH. 
Configure a daily recurring (or more often) execution time in the timer configuration and deploy the Iflow. Done.

Download the zip by clicking on the release on the right side.
