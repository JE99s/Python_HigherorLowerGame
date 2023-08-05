<h1>Creating a Higher or Lower Game with Python</h1>
Small simple version of the Higher or Lower Game utilizing Python.
<h2>Description</h2>
<p>I enjoyed playing the Higher or Lower Game to test myself if I unnecessarily know who or what gets searched up more on Google. I want to create my own simple version of the game utilizing Python. This project will help me develop my skill in grabbing a big problem and administering it into smaller chunks to complete.</p>
<br/>
<h2>Utilities Used</h2>

- <b>replit.com</b>
- <b>Python</b>

<h2>Environments Used</h2>

- <b>Web browser</b>
<h2>Preparation</h2>
Firstly, I decide on my programming environment. An online IDE named replit.com. Replit is a free online IDE that provides repositories to code anything from Python to Ruby. I’ve used this online environment before when learning Python and Java for the first time. It’s a great alternative to holding my project. Furthermore, Replit provides its own clear function which means that while code is running the screen can be cleared from a method imported from its own Repl compiler.
<br/>
<img src="https://i.imgur.com/wgr3cN1.png" height="75%" width="75%" alt="Linux command line steps"/>
<br />

<h3>Code</h3>
For this game, I want to be able to have two objects, the user to view information about them, and for the user to guess which one has the higher follower count. These three different goals are going to need three different Python files. I’ll create a logical draft of each <b>.py</b> file for the project.
<br/>
The project will contain three .py files: 

main.py – the functionality of the code 

art.py – the art of the code 

data.py – the database of the program where all data for comparable entities or objects will be placed. (e.g., Name, description, country, Instagram followers)

Here I want an ASCII type of art for my logo of the Higher or Lower Game. I want it to be simple. After a few attempts and a few pieces of paper, here is a drawing of what I have in mind for the logo of the game.
<br />
<img src="https://i.imgur.com/zhgbGc1.png" height="75%" width="75%" alt="Linux command line steps"/>
<br />
Back on my Kali Linux VM, in the same MS2 web server, I will click the Mutillidae link, and it takes me to the Mutillidae website page. I click <b>OWASP Top 10 > A1 - Injection > SQLi - Extract Data > User Info</b>. As shown in the error-based SQL injection video gracefully made by NFE Systems Ltd. To get into a SQL injection you should start by entering special or reserved characters in the user name field to produce SQL syntax errors to exploit. Following along with the video instructions I made my own list of special reserved characters in a <b>.txt</b> document, as shown below.
<br/>
<img src="https://i.imgur.com/zXARBmZ.png" height="75%" width="75%" alt="Linux command line steps"/>
<br />
I enter all the special reserved characters on <b>line 1</b> of the <b>.txt</b> document into the Name field on the User Info page via copy and paste. I click the <b>View Account Details</b> button to submit the credentials.
<br/>
<img src="https://i.imgur.com/mQ0zjCS.png" height="75%" width="75%" alt="Linux command line steps"/>
<br />
I received an error message detailing the error in executing query. There is an error in SQL syntax and the message tells me that this database or server is running in MySQL. There’s also the SELECT statement set query that’s running in the background. I want to copy all contents inside the <b>Diagnostic Information</b> field and paste that into another <b>.txt</b> document.
<br/>
<img src="https://i.imgur.com/Foa77GA.png" height="75%" width="75%" alt="Linux command line steps"/>
<br />
Notice the SELECT statement. This is what happens inside the logs of the server when users log in.  Inside the bottom Mousepad window, the statement underlined in red is my input from earlier which is provided in the Mousepad document above as well. That is what I have control of, and the SELECT statement is what the website does to retrieve data from its SQL server. For this injection, I need to get this SELECT statement to always be true. So, on <b>line 3</b> I type ‘ or “a”=”a”.
<br/>
<img src="https://i.imgur.com/5lLiyNP.png" height="75%" width="75%" alt="Linux command line steps"/>
<br />
Now the statement tells us that <b>Select *</b> (all columns) <b>From accounts where username</b> is equal to ‘(nothing) or a equals a. We know that “a” is always going to be equal to “a”, so that statement provides a true statement that I’m looking for. The bit at the bottom with the single quotes and password equals ‘ ‘ needs to be commented out.
<br/>
<img src="https://i.imgur.com/D2Md9e0.png" height="75%" width="75%" alt="Linux command line steps"/>
<br />
I put a # (hash) at the end of <b>line 3</b> which will comment out the rest of the line giving me what I’m looking for. Now, I can try to attempt the attack again by this time entering the contents of <b>line 3</b> back into the <b>Name</b> field on the login page provided by the User Info page. I press the <b>View Account Details</b> button and now I can see 16 records and their respective usernames, passwords, and signatures all dumped on the page.
<br/>
<img src="https://i.imgur.com/93oufVv.png" height="80%" width="80%" alt="Linux command line steps"/>
<br />
