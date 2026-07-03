# Prevent-error-based-SQL-injection
Preventing error-based SQL injection involves preparing statements.

Click Windows Start and select File Explorer.

<img width="470" height="824" alt="image" src="https://github.com/user-attachments/assets/206f3dd3-b9af-497c-a859-210e5f4a9769" />

Under Quick Access, open error-sql.

<img width="704" height="479" alt="image" src="https://github.com/user-attachments/assets/e6321461-d311-41ce-bcee-1d4efb2c2417" />

Double-click process.php to open the file and view the code.

The PHP code takes input for username and password.

$username = $_POST['username'];

$password = $_POST['password'];

The input is saved to a file.

fwrite($file, $username);

The SQL statement selects all data for the user with the given username.

$sql = "SELECT * FROM users WHERE user='$username'";

<img width="608" height="491" alt="image" src="https://github.com/user-attachments/assets/908178c6-905c-48cf-98dd-fc16814468ca" />

Close the file and open Updated Files in the File Explorer window.

<img width="772" height="547" alt="image" src="https://github.com/user-attachments/assets/a0123ae4-cae4-45b3-a097-4192296c16fd" />

Open process.php to view the code.

The updated code uses real_escape_string to prevent special characters from being executed. The SQL statement uses a prepared statement instead of being directly run to prevent SQL injection.

<img width="685" height="464" alt="image" src="https://github.com/user-attachments/assets/0e36c48b-e987-449f-ac6f-178495162489" />

Open the error-sql folder and paste the copied file.

Click Replace the file in the destination.

<img width="445" height="298" alt="image" src="https://github.com/user-attachments/assets/0c096cc5-d0cb-4d09-8cc9-f089d8d31a68" />

Switch back to the Error-based SQL web page. In the Username box, enter:

' or 1=1#

<img width="297" height="178" alt="image" src="https://github.com/user-attachments/assets/86e5f02f-973c-4636-8da1-582c041d7036" />

The input is read as plaintext instead of SQL, so the page does not return every user's information.

<img width="291" height="54" alt="image" src="https://github.com/user-attachments/assets/ecda6714-6ea2-476e-b349-f2e18205add4" />





