# 4ACTIVE Software Requirement Specification (SRS)

|     |     |
| --- | --- |
| **Target release** | Type // to add a target release date |
| **Epic** | Type /Jira to add Jira epics and issues |
| **Document status** | DRAFT |
| **Document owner** | @ mention owner |
| **Designer** | @ designer |
| **Tech lead** | @ lead |
| **Technical writers** | @ writers |
| **QA** |     |

## Objective

The objective of this Software Requirements Specification (SRS) document is to outline the functional and non-functional requirements for a gym class management web application. This project serves as a sample demonstration of my skills in manual testing and requirements analysis.

The requirements detailed in this document are based on a real-world website, [4-active.pl](https://4-active.pl/grafik-zajec/fitness), specifically focusing on their class scheduling functionality. This SRS provides a framework for understanding the expected features and behaviors of the application, showcasing my ability to translate user needs into actionable specifications.

By presenting this sample project, I aim to illustrate my proficiency in developing technical documentation that can guide the development and testing processes.

## Assumptions

*   Users have internet access.
    

## Requirements

| Epic (Total: 2) |     | Requirement (Total: 8) |     |     |
| --- | --- | --- | --- | --- |
| Key | Summary | Key | Summary | Description |
| --- | --- | --- | --- | --- |
| [AV-13](https://mohammed-tayeb.atlassian.net/browse/AV-13) | Admin Class Management | [AV-11](https://mohammed-tayeb.atlassian.net/browse/AV-11) | Add Classes to Gym Schedule | As an admin user, I can add classes to the schedule so that members can view and sign up for them.<br><br>*   I must provide the following details.<br>    *   The name of the class.<br>    *   The date and time of the class.<br>    *   The instructor's name.<br>    *   The number of available spaces for participants.<br>*   When I add a new class, the new class information should be reflected in the gym schedule immediately.<br>*   If the operation is successful, a confirmation message should be displayed to inform me that the class details have been added.<br>*   If there are validation errors (e.g., overlapping class times), an error message should inform me of the issue, preventing the changes from being saved. |
| [AV-10](https://mohammed-tayeb.atlassian.net/browse/AV-10) | Delete Classes from Gym Schedule | As an admin user, I can delete existing classes from the schedule so that outdated or canceled classes are removed and members see only relevant information.<br><br>*   When I choose to delete a class, I must be prompted with a confirmation message to confirm the deletion.<br>*   If I confirm the deletion, the class should be removed from the schedule immediately.<br>*   A success message should be displayed to inform me that the class has been deleted successfully.<br>*   All registered users must receive an email notification informing them that the class has been canceled, including:<br>    *   The name of the canceled class.<br>    *   The original date and time of the class.<br>    *   A message encouraging them to check the schedule for other available classes.<br>*   If there are any issues with the deletion (e.g., the class cannot be deleted due to ongoing registrations), an error message should inform me of the reason. |
| [AV-9](https://mohammed-tayeb.atlassian.net/browse/AV-9) | Edit Existing Classes in Schedule | As an admin user, I can edit existing classes within the schedule so that members have access to the most up-to-date information regarding class details.<br><br>*   I must be able to modify the following details:<br>    *   The name of the class.<br>    *   The date and time of the class.<br>    *   The instructor's name.<br>    *   The number of available spaces.<br>*   When I save the changes, the updated information should be reflected in the gym schedule immediately.<br>*   If the updates are successful, a confirmation message should be displayed to inform me that the class details have been updated.<br>*   If there are validation errors (e.g., overlapping class times), an error message should inform me of the issue, preventing the changes from being saved. |
| [AV-12](https://mohammed-tayeb.atlassian.net/browse/AV-12) | Gym Class Scheduling and Registration | [AV-8](https://mohammed-tayeb.atlassian.net/browse/AV-8) | Prevent Subscribing to Past Classes | As a logged-in gym user, if I attempt to subscribe to a class that has already occurred, I should receive a pop-up message informing me that the date has passed and subscription is not allowed. |
| [AV-7](https://mohammed-tayeb.atlassian.net/browse/AV-7) | Login Prompt for Unauthenticated Users | As a user who is not logged in, if I attempt to sign up for a class, a pop-up message should appear prompting me to log in first. |
| [AV-6](https://mohammed-tayeb.atlassian.net/browse/AV-6) | Unsubscribe from Classes | As a logged-in gym user, I want to unsubscribe from a class up to 2 hours before it starts to manage my schedule. Upon successful cancellation, I should receive a confirmation pop-up. If I try to unsubscribe within 2 hours of the class start time, a message should inform me that cancellations are not allowed. |
| [AV-5](https://mohammed-tayeb.atlassian.net/browse/AV-5) | Class Signup for Registered Users | As a logged-in gym user, I want to be able to sign up for a class that still has available spots. If I attempt to register for a class that is full, a pop-up notification should inform me that the class is at capacity, preventing me from signing up. |
| [AV-4](https://mohammed-tayeb.atlassian.net/browse/AV-4) | View Gym Schedule | As any user (logged in or not), I want to view the gym schedule to see all available classes and their details. The schedule should display the following information for each class:<br><br>*   Class name<br>*   Date and time<br>*   Instructor's name<br>*   Number of available spots |

## User interaction and design

1.  Sample class schedule, available to view by any user.
    

![image-20240923-115526.png](./attachments/image-20240923-115526.png)

2.  Pop-up to sign up for a class
    

![image-20240923-115631.png](./attachments/image-20240923-115631.png)

4.  Login prompt for unauthenticated users
    

![image-20240923-115916.png](./attachments/image-20240923-115916.png)

5.  Class Signup for registered users (no available seats)
    

![image-20240923-120723.png](./attachments/image-20240923-120723.png)

6.  Class Signup for registered users (available seats)
    

![image-20240923-121204.png](./attachments/image-20240923-121204.png)

7.  Unsubscribe from Classes
    

![image-20240923-121346.png](./attachments/image-20240923-121346.png)

8.  Prevent Subscribing to Past Classes
    

![image-20241002-164543.png](./attachments/image-20241002-164543.png)