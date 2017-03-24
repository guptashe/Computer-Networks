# Computer-Networks
CS5700
INTRODUCTION
---------------------
This project is about a client program which connects to the server and works as a web crawler. Web crawler is a piece of software that automically gathers
and traverses secet flags on the website Fakebook.Once the client is connected to the server, it captures the request and response and depending on the status
codes its behaves further. When the status code is OK it moves forward to traverse the web, going through each link in search of 5 hiden secret flags. after
receiving the flag, the client should stop traversing.

HIGH LEVEL APPROACH
-------------------------------
We have scripted this code in Python 2.7
1. Import the required packages like socket, re & Sys
2. Defined two methods which takes arguments like username and password
3. Created a TCP socket connection
4. When the socket is connected, the client sends a GET request, receives its response and extracts the sessionid and csrftoken.
5.The client extracts the csrftoken and sessionid using the regular expression method.
6. Now the client sends the POST request with the session parameters for login and receives the login page using GET method.
7. The program starts traversing on the received page searching for the flags colored in red as well as the regex sarches for the urls.
8. It keeps the count of visited urls and unvisited urls so that the program doesn't enter into loop.
9. We have provided conditions for various status codes, which the program extracts from the Header of response message.
10. Provided validations for not letting the program enter the loop.


CHALLENGES FACED
---------------------------
1. Handling the response message sent by server and login into the Fakebook account.
2. Extracting the session id and csrf token from the response message.
3. Extracting the urls from the response message.
4. Avoiding the program from entering the loop
5. Collecting the flags

OVERVIEW OF CODE TESTING
---------------------------------------
1. Tested the code by checking the different response code obtained by the server.
2. Tested the code for exception handling for invalid inputs.
3. Tested the code on the ccis machine using makefile by remote login.

DELIVERABLES
-------------------
1. webcrawler
2. Makefile
3. README.txt
4. secret_flags
