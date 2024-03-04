# Weight-Tracking-App
A simple Android app used to track weight, calorie intake, and your progress over time

The goal of this app is to act as base code to build up from. So far the 'Project3.zip' has a built in login screen that allows a user to create an account and sign in to access the app. As of current the app isn't yet completed but the additional zip file named 'TylerStricklandWeightApp.zip', the display file, has the baseline of the UI that I plan to implement, but none of the working code.

The screen the app opens to is the login screen, which can also direct the user to the sign up screen. Once the user signs up and then logs in, assuming their credentials match, they can access the app main screen. The primary screen would have a visual on the top that indicates how many calories the user has left in the day via a filling strawberry as seen in the display file. On the bottom half of the main screen is the graph that would show both the user weight over a set period of time and a rough showing of how mawny calories over or under they've eaten per day. This screen would also have a popup upon entering the first time that asks a user if they'd like to recieve SMS notifications reminding them of tracking their weight or certian time sin the day when they'd usually have their meals to record their calories and how many they have left.

I coded the login screen only so far, having used SQLite for the first time to create a database. I only implemented a create and read fucntionality because most apps don't delete user credentials unless it's been an extended period of time of their account being inactive. My strategy for coding this part of the work was to work on the backend first then create the visual to go along with it afterward. So I started with setting up the database helper class first that would create the database if it didn't exist and if it did to then access it. Once that was figured out I worked on accepting user inputs into the database, implementing the sign up screen first and checking that the database did accept the inputs as expected. Finally, I had to create a read fucntion that would take the input on the login screen and cross reference witht he database to verify if any users matched the username and password for the account. An email and many more credentials could be easily ipmlemented by just adding another column and input to the sign in screen or by doing it in app, but for the base functionality of the app this was the very least needed for it to be funcitonal. To test the code I input different variables in the sign up screen to ensure the databse reflected it correctly and then tested the login screen by having it redirect to the main screen if the login was successful.

The most difficult part was working with the database as this is the first time I'm doing anything with creating databases in Android Studio. But once the read and create functions were created it practically serviced itself, only having to make sure the inputs were accurate and were being accepted. Something I could work on in the future is preventing duplicates of usernames and if the app was to be planned to go live a password reset function (which would require an external form of contact, a secured random number generated code sent to them, and cross referencing the code then allowing the user to update their password).
