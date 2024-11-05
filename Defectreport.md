# Defect report

##### **Introduction**

This section contains a detailed defect report for three identified bugs
during test execution demonstrating to show how to capture a bug detail
if there were any on the 4active.pl website. Each bug report includes
the following information:

- **Overview**: A brief description of the bug.

- **Steps to Reproduce**: A clear, step-by-step guide on how to
  replicate the bug.

- **Expected Results**: What should happen under normal conditions.

- **Actual Results**: The actual outcome when the bug occurs.

- **Impact on Users**: An assessment of how each bug affects user
  experience and functionality.

- **Affected Version**: The version of the application where the bug was
  found.

- **Fixed Version**: The version where the bug was resolved.

- **Assignee**: The team member responsible for addressing the bug.

- **Reporter**: The name of the individual who reported the bug.
  
  

This documentation showcases my capability to identify and articulate
software defects.

# 

<table>
<colgroup>
<col style="width: 6%" />
<col style="width: 16%" />
<col style="width: 29%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 13%" />
<col style="width: 13%" />
</colgroup>
<thead>
<tr>
<th colspan="7" style="text-align: center;"><strong>Bug (Total:
3)</strong></th>
</tr>
<tr>
<th style="text-align: center;"><strong>Key</strong></th>
<th style="text-align: center;"><strong>Summary</strong></th>
<th style="text-align: center;"><strong>Description</strong></th>
<th style="text-align: center;"><strong>Affects versions</strong></th>
<th style="text-align: center;"><strong>Fix versions</strong></th>
<th style="text-align: center;"><strong>Assignee</strong></th>
<th style="text-align: center;"><strong>Reporter</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-3">AV-3</a></td>
<td>No confirmation pop-up after successful class unsubscription</td>
<td><h3 id="overview">Overview</h3>
<p>When a logged-in gym user unsubscribes from a class scheduled to
start in 3 hours, the expected confirmation pop-up does not appear. This
lack of feedback may lead users to believe the unsubscription action was
unsuccessful.</p>
<h3 id="steps-to-reproduce">Steps to Reproduce:</h3>
<ol type="1">
<li><p>Log in as a gym user with valid credentials.</p></li>
<li><p>Book a class that is scheduled to start in 3 hours.</p></li>
<li><p>Go to the class schedule.</p></li>
<li><p>Choose to unsubscribe from the booked class.</p></li>
<li><p>Confirm the unsubscription.</p></li>
</ol>
<h3 id="expected-result">Expected Result:</h3>
<p>A confirmation pop-up should appear with the message: "You have
successfully unsubscribed from the class."</p>
<h3 id="actual-result">Actual Result:</h3>
<p>No confirmation pop-up appears after the class is successfully
unsubscribed.</p>
<h3 id="impact">Impact:</h3>
<p>The absence of the confirmation message may cause confusion, as users
may think the action did not complete successfully.</p></td>
<td>1.0</td>
<td>1.1</td>
<td>Mohammed Tayeb</td>
<td>Mohammed Tayeb</td>
</tr>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-2">AV-2</a></td>
<td>Confirmation Pop-up Not Displaying After Unsubscribing</td>
<td><h3 id="overview-1">Overview</h3>
<p>When a logged-in gym user unsubscribes from a class that is scheduled
to start in more than 2 hours, the expected confirmation pop-up does not
appear. As a result, the user is left without feedback or confirmation
that the action has been successfully completed.</p>
<h3 id="steps-to-reproduce-1">Steps to Reproduce:</h3>
<ol type="1">
<li><p>Log in as a gym user with valid credentials.</p></li>
<li><p>Navigate to the "My Classes" page where booked classes are
displayed.</p></li>
<li><p>Select a class that is scheduled to start in 3 hours.</p></li>
<li><p>Click on the "Unsubscribe" button next to the selected
class.</p></li>
</ol>
<h3 id="expected-result-1">Expected Result:</h3>
<ul>
<li><p>A confirmation pop-up should appear stating: <strong>"You have
successfully unsubscribed from the class."</strong></p></li>
<li><p>The class should be removed from the user's booked classes
list.</p></li>
</ul>
<h3 id="actual-result-1">Actual Result:</h3>
<ul>
<li><p>The confirmation pop-up does not appear after clicking the
"Unsubscribe" button.</p></li>
<li><p>The class is still removed from the list, but there is no user
feedback or confirmation of the action.</p></li>
</ul>
<h3 id="impact-1">Impact:</h3>
<ul>
<li><p>Users may think that the unsubscribe action was unsuccessful
because of the missing confirmation message, leading to confusion or
attempts to reattempt the action unnecessarily.</p></li>
</ul></td>
<td>1.0</td>
<td>1.1</td>
<td>Mohammed Tayeb</td>
<td>Mohammed Tayeb</td>
</tr>
<tr>
<td><a
href="https://mohammed-tayeb.atlassian.net/browse/AV-1">AV-1</a></td>
<td>Edited class details not saving or reflecting in gym schedule</td>
<td><h3 id="overview-2">Overview</h3>
<p>This defect occurs when an admin user edits the details of a class on
the gym schedule page. Although a confirmation message appears, the
updated class details are not reflected in the schedule, and the
original information remains unchanged even after refreshing the
page.</p>
<p><strong>Steps to Reproduce</strong>:</p>
<ol type="1">
<li><p>Log in as an admin user.</p></li>
<li><p>Navigate to the gym schedule page.</p></li>
<li><p>Select an existing class to edit.</p></li>
<li><p>Modify the class details with the following:</p>
<ul>
<li><p><strong>Class name</strong></p></li>
<li><p><strong>Date and time</strong></p></li>
<li><p><strong>Instructor's name</strong></p></li>
<li><p><strong>Available spaces</strong></p></li>
</ul></li>
<li><p>Click the "Save" button.</p></li>
</ol>
<h3 id="expected-result-2">Expected Result:</h3>
<ul>
<li><p>The updated class details should be reflected in the gym
schedule.</p></li>
<li><p>A confirmation message should appear, indicating that the class
details have been successfully updated.</p></li>
</ul>
<h3 id="actual-result-2">Actual Result:</h3>
<ul>
<li><p>After saving the changes, the confirmation message "Class details
have been updated" is displayed, but the class details are not updated
in the gym schedule. The original information remains
unchanged.</p></li>
<li><p>Refreshing the page does not resolve the issue.</p></li>
</ul>
<h3 id="impact-2">Impact:</h3>
<p>Admins may mistakenly believe that the class details were
successfully updated, potentially causing scheduling conflicts or
miscommunication with gym members.</p></td>
<td>1.0</td>
<td>1.1</td>
<td>Mohammed Tayeb</td>
<td>Mohammed Tayeb</td>
</tr>
</tbody>
</table>
