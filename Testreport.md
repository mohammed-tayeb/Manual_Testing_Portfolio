# Test Report



# Introduction

This test report documents the testing activities conducted on the
**4active.pl** website, specifically focusing on the features outlined
in the Software Requirements Specification (SRS). The scope is limited
to functionalities defined in the SRS rather than all the
functionalities that 4active website offers.

The testing approach within this document includes both **Gherkin-based
scenarios** and **manual test steps** to demonstrate my familiarity with
both methods. Additionally, a few test cases were intentionally marked
as "Failed" to show the reporting process when defects are identified.
As a result of these failed test cases, a separate **Defect Report** was
created with the bugs discovered during testing. Please note that these
bugs were created only for the purpose of this portfolio and do not
reflect any actual issues on the 4active website.

#### Report Structure:

Each test entry is organized as follows:

- **Test Case ID:** uniquely identifies the test case

- **Fix Versions:** Indicates applicable version for fixes.

- **Test Case Description:** Brief description of the scenario being
  tested.

- **Linked Issues:** Any related issues or requirements.

- **Test Execution ID:** Identifier for tracking the specific test
  execution.

- **Test Result:** Outcome of the test (Passed/Failed).

- **Start and End Dates:** Duration of the test execution.

- **Tester:** Tester’s name.

- **Test Environment:** Details on the environment configuration.

- **Test Version:** Version of the system under test.

- **Test Steps:** Steps are detailed in either Gherkin syntax or as
  manual steps based on the scenario.
  
  
  ###### This report serves as evidence of my skills in documenting, executing, and reporting test outcomes, as well as managing and communicating defect findings.
  
  

## [AV-25](https://mohammed-tayeb.atlassian.net/browse/AV-25) Verify Gym Schedule Visibility

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                                                                               |
|:-----------------:| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Description**   | This test case ensures that all users, whether logged in or not, can access the gym schedule and view essential class details, including class name, date, time, instructor, and available spots. |
| **Linked Issues** | tests [AV-4](https://mohammed-tayeb.atlassian.net/browse/AV-4) View Gym Schedule                                                                                                                  |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 03:32 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-02 10:58 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in or not 4active.pl<br />
When I navigate to the gym schedule page<br />
Then I should see the following class details<br />
| class name | date | time | instructor | available spots |<br />
| Yoga | 2024-09-24 | 10:00 | Alice Johnson | 5 |<br />
| Spinning | 2024-09-24 | 12:00 | Bob Smith | 3 |<br />
| Pilates | 2024-09-25 | 14:00 | Cathy Lee | 7 |<br />
| Zumba | 2024-09-25 | 16:00 | David Wilson | 0 |</td>
</tr>
</tbody>
</table>

## [AV-24](https://mohammed-tayeb.atlassian.net/browse/AV-24) Verify Class Sign-Up Functionality for Registered Users

## Manual

| **Fix versions**  | 1.1                                                                                                                                                                                                              |
|:-----------------:| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Description**   | This test case ensures that logged-in gym users can sign up for classes with available spots. It also verifies that a notification appears when attempting to register for a full class, preventing the sign-up. |
| **Linked Issues** | tests [AV-5](https://mohammed-tayeb.atlassian.net/browse/AV-5) Class Signup for Registered Users                                                                                                                 |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 03:34 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 03:34 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

## Steps

| **Step \#** | **Action**                                                                     | **Data**           | **Expected Result**                                                   | **Actual Results** | **Comment** | **Defects** | **Step State** |
|:-----------:| ------------------------------------------------------------------------------ | ------------------ | --------------------------------------------------------------------- | ------------------ | ----------- | ----------- | -------------- |
| **1**       | I open the 4active website and I log in                                        | www.4active.com    | Page opens and log in is successful                                   |                    |             |             | PASSED         |
| **2**       | I click on a class that has available spots                                    | e.g., Active Cross | A pop-up is displayed, confirming the sign up                         |                    |             |             | PASSED         |
| **3**       | On the pop-up, I click "Sign up" to confirm that I am signing up for the class |                    | Pop-up message displayed confirming that I am signed up for the class |                    |             |             | PASSED         |

## [AV-23](https://mohammed-tayeb.atlassian.net/browse/AV-23) Verify Unsubscribe Functionality with Confirmation Pop-Up

## Cucumber

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 84%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Fix versions</strong></th>
<th>1.1</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;"><strong>Description</strong></td>
<td>This test case ensures that logged-in gym users can unsubscribe from
a class up to 2 hours before it starts and receive a confirmation pop-up
upon successful cancellation.</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Linked Issues</strong></td>
<td>created <a
href="https://mohammed-tayeb.atlassian.net/browse/AV-3">AV-3</a> No
confirmation pop-up after successful class unsubscription<br />
created <a
href="https://mohammed-tayeb.atlassian.net/browse/AV-2">AV-2</a>
Confirmation Pop-up Not Displaying After Unsubscribing<br />
tests <a
href="https://mohammed-tayeb.atlassian.net/browse/AV-6">AV-6</a>
Unsubscribe from Classes</td>
</tr>
</tbody>
</table>

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | FAILED                                                                                                       |
| **Started On**        | 2024-10-01 03:38 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 03:46 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in as a gym user<br />
And I have already booked a class that starts in <3> hours<br />
When I choose to unsubscribe from the class<br />
Then I should see a confirmation pop-up saying "You have successfully
unsubscribed from the class."</td>
</tr>
</tbody>
</table>

## [AV-22](https://mohammed-tayeb.atlassian.net/browse/AV-22) Verify Login Prompt on Class Sign-Up Attempt for Unauthenticated Users

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                         |
|:-----------------:| ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Description**   | This test case ensures that unauthenticated users receive a pop-up message prompting them to log in when attempting to sign up for a class. |
| **Linked Issues** | tests [AV-7](https://mohammed-tayeb.atlassian.net/browse/AV-7) Login Prompt for Unauthenticated Users                                       |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 03:30 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 03:30 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

## Iterations

Iteration 1 -

Yoga

PASSED

Iteration 2 -

Cross fit

PASSED

Iteration 3 -

Zumba

PASSED

Iteration 4 -

Judo

PASSED

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am not logged in<br />
When I navigate to the gym schedule page<br />
And I attempt to sign up for a class <class><br />
Then a login prompt should appear<br />
And I should be asked to log in before signing up for the class<br />
Examples:<br />
| class |<br />
| Yoga |<br />
| Cross fit |<br />
| Zumba |<br />
| Judo |</td>
</tr>
</tbody>
</table>

## [AV-21](https://mohammed-tayeb.atlassian.net/browse/AV-21) Verify Subscription Prevention for Past Classes

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                                                                                                  |
|:-----------------:| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Description**   | This test case ensures that logged-in gym users receive a pop-up message when attempting to subscribe to a class that has already occurred, informing them that the date has passed and subscription is not allowed. |
| **Linked Issues** | tests [AV-8](https://mohammed-tayeb.atlassian.net/browse/AV-8) Prevent Subscribing to Past Classes                                                                                                                   |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 03:26 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 03:26 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in<br />
And the current date is "2024-09-24"<br />
When I attempt to subscribe to a class that has already occurred<br />
Then a pop-up message should appear saying "The deadline to register for
classes has passed"<br />
And I should not be able to subscribe to the class</td>
</tr>
</tbody>
</table>

## [AV-20](https://mohammed-tayeb.atlassian.net/browse/AV-20) Verify Cancellation Restriction for Unsubscribing Less Than 2 Hours Prior to Class Start

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                                                                                 |
|:-----------------:| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Description**   | This test case ensures that logged-in gym users receive a message informing them that cancellations are not allowed when attempting to unsubscribe less than 2 hours prior to the class start time. |
| **Linked Issues** | tests [AV-6](https://mohammed-tayeb.atlassian.net/browse/AV-6) Unsubscribe from Classes                                                                                                             |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 03:56 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 03:56 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in as a gym user<br />
And I have already booked a class that starts in less than 2 hours<br />
When I try to unsubscribe from the class<br />
Then I should see a message saying "Cancellations are not allowed within
2 hours of the class start time."</td>
</tr>
</tbody>
</table>

## [AV-19](https://mohammed-tayeb.atlassian.net/browse/AV-19) Verify Overlap Error for New Class Addition

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                                                                                                     |
|:-----------------:| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Description**   | This test case ensures that when an admin attempts to add a new class with a time that conflicts with an existing class. The system displays an error message about the overlap, preventing the class from being saved. |
| **Linked Issues** | tests [AV-11](https://mohammed-tayeb.atlassian.net/browse/AV-11) Add Classes to Gym Schedule                                                                                                                            |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 03:58 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 03:58 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in as an admin user<br />
And I am on the gym schedule page<br />
And there is an existing class at "2024-10-10 6:00 PM"<br />
When I fill in the class details with:<br />
| Field | Value |<br />
| Class name | "Yoga Class" |<br />
| Date and time | "2024-10-10 6:00 PM" | # Overlaps with existing
class<br />
| Instructor's name | "Bob Smith" |<br />
| Available spaces | 20 |<br />
And I save the new class<br />
Then I should see an error message indicating "Class times overlap with
an existing class."</td>
</tr>
</tbody>
</table>

## [AV-18](https://mohammed-tayeb.atlassian.net/browse/AV-18) Verify Class Addition Functionality for Admin Users

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                                                                                                                              |
|:-----------------:| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Description**   | This test case ensures that admin users can add new classes to the gym schedule by providing the required details, and that the class information is immediately reflected in the schedule with a confirmation message upon successful addition. |
| **Linked Issues** | tests [AV-11](https://mohammed-tayeb.atlassian.net/browse/AV-11) Add Classes to Gym Schedule                                                                                                                                                     |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 03:59 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 03:59 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in as an admin user<br />
And I am on the gym schedule page<br />
When I fill in the class details with:<br />
| Field | Value |<br />
| Class name | "Zumba Class" |<br />
| Date and time | "2024-10-10 6:00 PM" |<br />
| Instructor's name | "Alice Johnson" |<br />
| Available spaces | 25 |<br />
And I save the new class<br />
Then the new class should be reflected in the gym schedule<br />
And I should see a confirmation message indicating the class has been
added</td>
</tr>
</tbody>
</table>

## [AV-17](https://mohammed-tayeb.atlassian.net/browse/AV-17) Verify Failure to Delete Class Due to Ongoing Registrations

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                                                                                    |
|:-----------------:| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Description**   | This test case verifies that when an admin attempts to delete a class with ongoing registrations, they receive a confirmation message, and upon confirming the deletion, an error message is displayed |
| **Linked Issues** | tests [AV-10](https://mohammed-tayeb.atlassian.net/browse/AV-10) Delete Classes from Gym Schedule                                                                                                      |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 04:09 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 04:09 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in as an admin user<br />
And I am on the gym schedule page<br />
When I select a class with ongoing registrations to delete<br />
Then I should see a confirmation message<br />
When I confirm the deletion<br />
Then I should see an error message indicating "Cannot delete the class
due to ongoing registrations."</td>
</tr>
</tbody>
</table>

## [AV-16](https://mohammed-tayeb.atlassian.net/browse/AV-16) Verify Successful Class Deletion and Notification to Users

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                                                                                                                                                                                                                     |
|:-----------------:| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Description**   | This test case verifies that an admin can successfully delete a class from the schedule. It ensures that a confirmation prompt is displayed, the class is removed, a success message is shown, and all registered users receive an email notification containing the class details and a reminder to check for other available classes. |
| **Linked Issues** | tests [AV-10](https://mohammed-tayeb.atlassian.net/browse/AV-10) Delete Classes from Gym Schedule                                                                                                                                                                                                                                       |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 04:09 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 04:09 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in as an admin user<br />
And I am on the gym schedule page<br />
When I select a class to delete<br />
Then I should see a confirmation message<br />
When I confirm the deletion<br />
Then the class should be removed from the schedule<br />
And I should see a success message indicating the class has been
deleted<br />
And all registered users should receive an email notification
with:<br />
| Field | Value |<br />
| Canceled class name | "Yoga Class" |<br />
| Original date and time | "2024-10-01 10:00 AM" |<br />
| Encouragement message | "Check the schedule for other available
classes." |</td>
</tr>
</tbody>
</table>

## [AV-15](https://mohammed-tayeb.atlassian.net/browse/AV-15) Verify Error When Editing Class Details Due to Validation Issues

## Cucumber

| **Fix versions**  | 1.1                                                                                                                                                                 |
|:-----------------:| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Description**   | This test case verifies that when an admin tries to save class details that conflict with another class time, an error message is displayed indicating the overlap. |
| **Linked Issues** | tests [AV-9](https://mohammed-tayeb.atlassian.net/browse/AV-9) Edit Existing Classes in Schedule                                                                    |

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | PASSED                                                                                                       |
| **Started On**        | 2024-10-01 04:01 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 04:01 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in as an admin user<br />
And I am on the gym schedule page<br />
And I have selected a class to edit<br />
When I modify the class details with:<br />
| Field | New Value |<br />
| Class name | "Yoga Class" |<br />
| Date and time | "2024-10-01 10:00 AM" | # Overlaps with another
class<br />
| Instructor's name | "Jane Smith" |<br />
| Available spaces | 15 |<br />
And I save the changes<br />
Then I should see an error message indicating "Class times overlap with
an existing class."</td>
</tr>
</tbody>
</table>

## [AV-14](https://mohammed-tayeb.atlassian.net/browse/AV-14) Verify Successful Editing of Class Details

## Cucumber

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 84%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Fix versions</strong></th>
<th>1.1</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;"><strong>Description</strong></td>
<td>This test case verifies that an admin can edit class details and
that changes are reflected immediately in the schedule, accompanied by a
confirmation message.</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Linked Issues</strong></td>
<td>created <a
href="https://mohammed-tayeb.atlassian.net/browse/AV-1">AV-1</a> Edited
class details not saving or reflecting in gym schedule<br />
tests <a
href="https://mohammed-tayeb.atlassian.net/browse/AV-9">AV-9</a> Edit
Existing Classes in Schedule</td>
</tr>
</tbody>
</table>

## Test Run Info

| **Test Execution**    | [AV-27](https://mohammed-tayeb.atlassian.net/browse/AV-27) Test Execution for Test Plan WEB-18 - version 1.0 |
|:---------------------:| ------------------------------------------------------------------------------------------------------------ |
| **Status**            | FAILED                                                                                                       |
| **Started On**        | 2024-10-01 04:03 PM GMT+00:00                                                                                |
| **Finished On**       | 2024-10-01 04:03 PM GMT+00:00                                                                                |
| **Executed By**       | Mohammed Tayeb                                                                                               |
| **Test environments** | Chrome-Windows10Pro                                                                                          |
| **Test Version**      | v1                                                                                                           |

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong>Gherkin</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Given I am logged in as an admin user<br />
And I am on the gym schedule page<br />
And I have selected a class to edit<br />
When I modify the class details with:<br />
| Field | New Value |<br />
| Class name | "Pilates Class" |<br />
| Date and time | "2024-10-05 11:00 AM" |<br />
| Instructor's name | "John Doe" |<br />
| Available spaces | 20 |<br />
And I save the changes<br />
Then the updated information should be reflected in the gym
schedule<br />
And I should see a confirmation message indicating the class details
have been updated</td>
</tr>
</tbody>
</table>
