# 4ACTIVE Software Requirement Specification (SRS)

<table>
<colgroup>
<col style="width: 34%" />
<col style="width: 65%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"><strong><br />
Target release</strong></th>
<th>Type // to add a target release date</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;"><strong>Epic</strong></td>
<td>Type /Jira to add Jira epics and issues</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Document status</strong></td>
<td>DRAFT</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Document owner</strong></td>
<td>@ mention owner</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Designer</strong></td>
<td>@ designer</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Tech lead</strong></td>
<td>@ lead</td>
</tr>
<tr>
<td style="text-align: center;"><strong>Technical writers</strong></td>
<td>@ writers</td>
</tr>
<tr>
<td style="text-align: center;"><strong>QA</strong></td>
<td></td>
</tr>
</tbody>
</table>

## Objective

The objective of this Software Requirements Specification (SRS) document
is to outline the functional and non-functional requirements for a gym
class management web application. This project serves as a sample
demonstration of my skills in manual testing and requirements analysis.

The requirements detailed in this document are based on a real-world
website, [4-active.pl](https://4-active.pl/grafik-zajec/fitness),
specifically focusing on their class scheduling functionality. This SRS
provides a framework for understanding the expected features and
behaviors of the application, showcasing my ability to translate user
needs into actionable specifications.

By presenting this sample project, I aim to illustrate my proficiency in
developing technical documentation that can guide the development and
testing processes.

## Assumptions

- Users have internet access.

## Requirements

<table>
<colgroup>
<col style="width: 6%" />
<col style="width: 16%" />
<col style="width: 6%" />
<col style="width: 20%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr>
<th colspan="2" style="text-align: center;"><strong>Epic (Total:
2)</strong></th>
<th colspan="3" style="text-align: center;"><strong>Requirement (Total:
8)</strong></th>
</tr>
<tr>
<th style="text-align: center;"><strong>Key</strong></th>
<th style="text-align: center;"><strong>Summary</strong></th>
<th style="text-align: center;"><strong>Key</strong></th>
<th style="text-align: center;"><strong>Summary</strong></th>
<th style="text-align: center;"><strong>Description</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-13">AV-13</a></td>
<td rowspan="3">Admin Class Management</td>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-11">AV-11</a></td>
<td>Add Classes to Gym Schedule</td>
<td><p>As an admin user, I can add classes to the schedule so that
members can view and sign up for them.</p>
<ul>
<li><p>I must provide the following details.</p>
<ul>
<li><p>The name of the class.</p></li>
<li><p>The date and time of the class.</p></li>
<li><p>The instructor's name.</p></li>
<li><p>The number of available spaces for participants.</p></li>
</ul></li>
<li><p>When I add a new class, the new class information should be
reflected in the gym schedule immediately.</p></li>
<li><p>If the operation is successful, a confirmation message should be
displayed to inform me that the class details have been added.</p></li>
<li><p>If there are validation errors (e.g., overlapping class times),
an error message should inform me of the issue, preventing the changes
from being saved.</p></li>
</ul></td>
</tr>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-10">AV-10</a></td>
<td>Delete Classes from Gym Schedule</td>
<td><p>As an admin user, I can delete existing classes from the schedule
so that outdated or canceled classes are removed and members see only
relevant information.</p>
<ul>
<li><p>When I choose to delete a class, I must be prompted with a
confirmation message to confirm the deletion.</p></li>
<li><p>If I confirm the deletion, the class should be removed from the
schedule immediately.</p></li>
<li><p>A success message should be displayed to inform me that the class
has been deleted successfully.</p></li>
<li><p>All registered users must receive an email notification informing
them that the class has been canceled, including:</p>
<ul>
<li><p>The name of the canceled class.</p></li>
<li><p>The original date and time of the class.</p></li>
<li><p>A message encouraging them to check the schedule for other
available classes.</p></li>
</ul></li>
<li><p>If there are any issues with the deletion (e.g., the class cannot
be deleted due to ongoing registrations), an error message should inform
me of the reason.</p></li>
</ul></td>
</tr>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-9">AV-9</a></td>
<td>Edit Existing Classes in Schedule</td>
<td><p>As an admin user, I can edit existing classes within the schedule
so that members have access to the most up-to-date information regarding
class details.</p>
<ul>
<li><p>I must be able to modify the following details:</p>
<ul>
<li><p>The name of the class.</p></li>
<li><p>The date and time of the class.</p></li>
<li><p>The instructor's name.</p></li>
<li><p>The number of available spaces.</p></li>
</ul></li>
<li><p>When I save the changes, the updated information should be
reflected in the gym schedule immediately.</p></li>
<li><p>If the updates are successful, a confirmation message should be
displayed to inform me that the class details have been
updated.</p></li>
<li><p>If there are validation errors (e.g., overlapping class times),
an error message should inform me of the issue, preventing the changes
from being saved.</p></li>
</ul></td>
</tr>
<tr>
<td rowspan="5"><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-12">AV-12</a></td>
<td rowspan="5">Gym Class Scheduling and Registration</td>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-8">AV-8</a></td>
<td>Prevent Subscribing to Past Classes</td>
<td>As a logged-in gym user, if I attempt to subscribe to a class that
has already occurred, I should receive a pop-up message informing me
that the date has passed and subscription is not allowed.</td>
</tr>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-7">AV-7</a></td>
<td>Login Prompt for Unauthenticated Users</td>
<td>As a user who is not logged in, if I attempt to sign up for a class,
a pop-up message should appear prompting me to log in first.</td>
</tr>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-6">AV-6</a></td>
<td>Unsubscribe from Classes</td>
<td>As a logged-in gym user, I want to unsubscribe from a class up to 2
hours before it starts to manage my schedule. Upon successful
cancellation, I should receive a confirmation pop-up. If I try to
unsubscribe within 2 hours of the class start time, a message should
inform me that cancellations are not allowed.</td>
</tr>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-5">AV-5</a></td>
<td>Class Signup for Registered Users</td>
<td>As a logged-in gym user, I want to be able to sign up for a class
that still has available spots. If I attempt to register for a class
that is full, a pop-up notification should inform me that the class is
at capacity, preventing me from signing up.</td>
</tr>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-4">AV-4</a></td>
<td>View Gym Schedule</td>
<td><p>As any user (logged in or not), I want to view the gym schedule
to see all available classes and their details. The schedule should
display the following information for each class:</p>
<ul>
<li><p>Class name</p></li>
<li><p>Date and time</p></li>
<li><p>Instructor's name</p></li>
<li><p>Number of available spots</p></li>
</ul></td>
</tr>
</tbody>
</table>

## User interaction and design

1. Sample class schedule, available to view by any user.

<img title="" src="file:///C:/Users/user/Downloads/image-20240923-115526.png" alt="" style="width:4.875in;height:1.96528in">

2. Pop-up to sign up for a class

<img src="./media/image2.tmp" style="width:4.875in;height:2.125in" />

4. Login prompt for unauthenticated users

<img src="./media/image3.tmp" style="width:4.875in;height:0.85417in" />

5. Class Signup for registered users (no available seats)

<img src="./media/image4.tmp" style="width:4.875in;height:2.16667in" />

6. Class Signup for registered users (available seats)

<img src="./media/image5.tmp" style="width:4.875in;height:0.72917in" />

7. Unsubscribe from Classes

<img src="./media/image6.tmp" style="width:4.875in;height:0.74306in" />

8. Prevent Subscribing to Past Classes

<img src="./media/image7.tmp"
style="width:3.57639in;height:2.51389in" />
