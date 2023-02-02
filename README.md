# Lab 2
[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repo and clone it to your machine to get started!

## Team Members
- Jessica Zhu
- No second team member

## Lab Question Answers 

### Evaluating TCP vs UDP
 Answer to Question 1: 
  After adding the loss, the reliability of the UDP significantly decreased. 
  Before adding the loss, all of the numbers 1-10 were correctly received in
  the order they were sent. After adding the loss, only some of the numbers
  were received. With the sending of the 1st sequence of 1-10, only the
  numbers 2, 3, 5, 6, 9, and 10 were received. With the sending of the 2nd
  sequence of 1-10, only the numbers 1, 2, and 8 were received. Finally, 
  with the sending of the 3rd sequence of 1-10, only the numbers 5, 9, and 
  10 were received.
  
  This occured because some of the information being sent, which was the
  sequence of numbers 1-10, was forced to be lost, so it did not reach the
  intended destination and wasn't received securely by the server. As UDP is
  connectionless, information is sent without the establishment of a secure
  connection. Thus, there is a chance that some of the information is lost, 
  which was the case when the 50% loss was added.
  
 Answer to Question 2:
  After adding the loss, the reliability of the TCP remained the same as all
  the numbers 1-10 were correctly received in the order they were sent. This 
  occured because TCP establishes an end to end connection, which means that
  all the information is sent in order from client to server. Even with the 
  forced loss being implemented, TCP has the capability to retransmit lost 
  data packets, guaranteeing the receipt of all the numbers 1-10. 
 
 Answer to Question 3:
  After adding the loss, the speed of the TCP response greatly slowed with
  each number taking almost 30 seconds before being displayed. Before the 
  loss, the TCP response was practically instantaneous. This occured because
  TCP extensively checks for connection reliability and acknowledges the 
  data packets being sent, resulting in delay when TCP determines there is 
  an error and the data packets are retransmitted.
  
 Sources for Questions 1-3:
  https://www.lifesize.com/blog/tcp-vs-udp/#:~:text=TCP%20is%20a%20connection%2Doriented,is%20only%20possible%20with%20TCP.
  
### TCP Client & Server
  Answer to Question 1:
   In the code, argc is an integer that holds the count for the number of
   arguments that have been passed via the command line. These arguments are
   stored in the argv array. This lets the user pass in arguments prior to
   the execution of the functions that call for those arguments.
   
  Answer to Question 2:
   A file descriptor is a unique number that is used to identify an open 
   file in the OS of a computer. This number is a non-negative integer. A 
   file descriptor table contains an array of integer file descriptors.
   
   Source for Question 2:
    https://www.computerhope.com/jargon/f/file--descriptor.htm 
    https://www.geeksforgeeks.org/input-output-system-calls-c-create-open-close-read-write/
    
  Answer to Question 3:
    A struct is a data type that the user defines so that a group of
    variables are associated with every use of the struct. For sockaddr_in,
    there are 2 declarations of the struct, serv_addr and cli_addr.
    
    Source for Question 3:
     https://www.geeksforgeeks.org/structures-c/
     
  Answer to Question 4:
    For the socket() function, there are 3 input parameters including int
    family, int type, and int protocol. In the code, the int family 
    parameter is AF_INET, which specifies the protocol family as IPV4. The 
    int type is SOCK_STREAM, which specifies a stream socket. Finally, the 
    int protocol is 0, which refers to the system default protocol. 
    
    The socket() function returns an integer socket descriptor that can be
    used in the future. If an error occurs, this integer is -1.
    
  Answer to Question 5:
    For the bind() function, there are 3 input parameters including int
    sockfd, struct sockaddr *my_addr, and int addrlen. The sockfd parameter 
    is the socket descriptor integer that was returned by the socket()
    function. In the code, the second parameter is serv_addr, which is a 
    pointer to struct sockaddr with the port and local IP address. Lastly,
    the int addrlen is set to the size of the struct sockaddr.
    
    For the listen() function, there are 2 input parameters including int
    sockfd, and int backlog. Again, the sockfd parameter is the socket
    descriptor. The int backlog parameter, which is defined as 5 in the 
    code, sets the number of allowed connections.
    
    Source for Questions 4-5:
     https://www.tutorialspoint.com/unix_sockets/socket_core_functions.htm#
     
  Answer to Question 6:
    The use of while(1) is implemented so that connections are executed one
    at a time in an ordered fashion where the code within the loop is run
    indefinitely. In this way, all the connections will be executed, however
    the loop does not allow for multiple connections to be executed at once.
    Therefore, this is a problem if there is a need for the execution of 
    multiple connections simultaneously since this loop cannot handle it.
    
  Answer to Question 7:
    The fork() command works by creating a new, child process that runs at 
    the same time as the original, parent process. Once the child process is
    created, both the child and parent processes execute later commands at
    the same time. This function does not take in any parameters and returns
    an integer. The integer is positive for the parent process, 0 for the 
    child process, or negative if an error occured. Here, the fork() command
    can be added so that a second connection can be executed within the loop
    at the same time as the first, allowing better handling of multiple
    connections due to the creation of the child process.
    
    Source for Question 7:
     https://www.geeksforgeeks.org/fork-system-call/
    
  Answer to Question 8:
    A system call is when a computer program interacts with the operating
    system (OS) by requesting a service from the kernel of the OS. These
    services are then provided to the program via APIs. Thus, in order for
    programs to interact with the kernel system, system calls are the only
    entry points.
    
    Source for Question 8:
    https://www.geeksforgeeks.org/introduction-of-system-call/

