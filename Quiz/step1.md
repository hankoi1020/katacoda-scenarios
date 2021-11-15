
## Database Privileges Quiz

>>Q1: What privilege should NOT grant to sale and manager?<<
=~= DROP ALL

>>Q2: Write a SQL statement to grant a privileges to ken@localhost so that ken can add new record in Company.customer<<
=== grant insert on Company.customer to 'ken'@'localhost';

>>Q3: Manager should have privilege to delete a database/table <<
( ) True
(*) False

>>Q4: How to see what privileges ken@localhost currently have? <<
=== show grants for 'ken'@'localhost';

>>Q5: How to remove ken privilege created in Q2? <<
=== revoke insert on Company.customer from 'ken'@'localhost'

## Markdown

<pre>
>>Q1: What privilege should NOT grant to sale and manager?<<
=~= DROP ALL

>>Q2: Write a SQL statement to grant a privileges to ken@localhost so that ken can add new record in Company.customer<<
=== grant insert on Company.customer to 'ken'@'localhost';

>>Q3: Manager should have privilege to delete a database/table <<
( ) True
(*) False

>>Q4: How to see what privileges ken@localhost currently have? <<
=== show grants for 'ken'@'localhost';

>>Q5: How to remove ken privilege created in Q2? <<
=== revoke insert on Company.customer from 'ken'@'localhost'
</pre>

The ***** within single and multiple choice indicates the correct answer. The syntax **===** is exact match, while **=~=** is a string containing match.

**Note:** There should not be a blank line between the question and the possible answers.

## Correct and Incorrect Answers

When a user clicks **Check Answers**, the correct answers will appear with a Green tick! If they have entered anything incorrect they will be asked to check and try again.

