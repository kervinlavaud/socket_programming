
CSC/CIS 419 Computer Networks
Programming Project: Palindrome Checker
About Palindrome:
https://en.wikipedia.org/wiki/Palindrome

Project Requirement:
	A team of two should perform this project. 
	It is required that one CSC person and one CIS person form a team.  
	It is suggested that CSC person is responsible for coding while CIS person is responsible for testing, project coordination, and writing the user manual. 
	All project code and documentation should be uploaded to Github (the shared link is required in your project report). Note: one Github link per team. The Github project must include the following content:
	All coding files should Include well-documented both PalindromeCheckerServer and PalindromeCheckerClient.  Be sure that the documentation correctly spells out the purpose of the code and carries your name. 
	A detailed user manual should include the descriptions of how to set up the program, installation environment, how to use the program, usage examples, and the testing results. (This manual is suggested to be written by CIS person and it is separated from your project report. The manual also needs to carry your name).
	Each individual should submit a project report. 
	The report must include but not limit to (1) what the project is? (2) how the project has been performed? (3) what your own contributions are? Or what you have done in the project?
	The project report is limited to 6 pages including figures and tables. 
	Text font size: 11; Normal margins; line spacing up to 1.15. 
	The project report should include a shared link created in Github that contains all materials for the project (e.g. code, testing result, network environment, etc.).  
	CSC person’s project report primarily highlights on the development and coding. It is suggested to have the following sections:
	Introduction of socket programming, may include the basic principles, the main procedures, the possible applications, and so forth.
	Methods used for your program, may include your design, flow chart, algorithm, data, etc.
	Experimental results in the final test that needs to coordinate/cooperate with CIS person.
	What is your own contribution/role in this project? Or what have you done in the project?
	A conclusion
	A shared Github link should be provided in the document. 
	CIS person’s project report should more highlight the information system and system management.  The CIS person’s documentation is suggested to have the following sections:
	Introduction of socket communication, may include the basic principles, the main procedures, the possible applications, and so forth.
	General introduction to methods used for your program that needs to coordinate/cooperate with CSC person for the details of development.
	Experimental environments, testing procedure, and results.
	What is your own contribution/role in this project? Or what have you done in the project?
	A conclusion
	A shared Github link should be provided in the document. 

Program Function Requirement:
	The client interacts with the user, collects a string, sends it to the server, and displays the response from the server
	The server receives a string from the client, determines if it is a palindrome or not, and sends a suitable response to the client
	A client and a server to handle strings and categorize them as palindromes and not palindromes

	Java/C++/C in Linux are recommended. Other programming language such as Python in Windows is also fine, but the documentation should be complete.

Optional Functions:
	Allow multiple threads. It means that the server can host connections from multiple clients simultaneously.  Server can identify and respond the requests from different clients.

Server-side Requirement:
1.	The server establishes its service on a port number supplied by the user (that can be assigned by the user from command line or user interface). For example, 

java PalindromeCheckerServer –port=1221

2.	The port number 1221 is used.  If no port option is used in the command line, the default port number 1200 is used.  Port numbers below 1024 are reserved for well-known applications and should not be used.  Further, if the port on which the service is started is already in use by another application, the program will terminate with an error message.  If the server is successful in establishing the Palindrome Checker service, it waits for connections from clients.

3.	The server can accept connections from several clients, but handling them one-by-one sequentially.  Each client may send a series of strings to be requested.  The server returns the results to the client.  

4.	The connection between the server and a client is closed when the client sends a null string to the server.  The server itself stops only when the process is terminated.  

Client-side Requirement:
1.	The client connects to a server on a specific port number supplied by the user in the command line or user interface.  For example, the client may connect to the Linux server holly.brockport.edu on port 1221.  
java PalindromeCheckerClient -port=1221 holly.brockport.edu
2.	If no port option is used in the command line, the default port number 1200 is used.  

3.	If no server is named in the command line, “localhost” is assumed. 

4.	PalindromeCheckerClient can interact with the user, accept strings, pass them on to the server for results, and prints out the results.  

5.	The client terminates when the user enters a null string (i.e., simply hits “Enter” key when prompted for an input string)

Testing Requirement:
	Must choose at least two tests from the below scenarios: Localhost test (standalone environment), SSH test (e.g. two accounts over SSH connection), Virtual Machine test (two VMs on a machine), and LAN test (physically two computers over LAN). The testing is suggested to be primarily conducted by CIS person.
	Screenshots ( .jpg, or .png) show (from the client side only) a series of strings submitted by a user to PalindromeCheckerClient with corresponding output. Include the following test cases (Capital letters, punctuation, and word dividers are allowed in a sentence palindrome):
	Acrobats stab orca
	poor guy dump
	23454032
	A man, a plan, a cat, a ham, a yak, a yam, a hat, a canal-Panama
	As I pee, sir, I see Pisa
	Air an aria.
	123454321
	Was it a car or a cat I saw

