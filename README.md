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
  sequence of 1-10, only the numbers 1, 2, and 8 were received. Finally, with
  the sending of the 3rd sequence of 1-10, only the numbers 5, 9, and 10 were
  received.
  
  This occured because some of the information being sent, which was the
  sequence of numbers 1-10, was forced to be lost, so it did not reach the
  intended destination and wasn't received securely by the server. As UDP is
  connectionless, information is sent without the establishment of a secure
  connection. Thus, there is a chance that some of the information is lost, 
  which was the case when the 50% loss was added.
  
 Answer to Question 2:
  After adding the loss, the realiability of the TCP remained the same as all
  the numbers 1-10 were correctly received in the order they were sent. This 
  occured because TCP establishes an end to end connection, which means that
  all the information is sent in order from client to server. Even with the 
  forced loss being implemented, TCP has the capability to retransmit lost 
  data packets, guaranteeing the receipt of all the numbers 1-10. 
 
 Answer to Question 3:
  After adding the loss, the speed of the TCP response greatly slowed with
  each number taking almost 30 seconds before being displayed. Before the 
  loss, the TCP response was practically instantaneous. This occured because
  TCP extensively checks for connection reliability and acknowledges the data
  packets being sent, resulting in delay when TCP determines there is an
  error and the data packets are retransmitted.
  
 Sources for Questions 1-3:
  https://www.lifesize.com/blog/tcp-vs-udp/#:~:text=TCP%20is%20a%20connection
  %2Doriented,is%20only%20possible%20with%20TCP.
  
### TCP Client & Server
  Answer to Question 1:
   In the code, argc is an integer...
  
 
 
