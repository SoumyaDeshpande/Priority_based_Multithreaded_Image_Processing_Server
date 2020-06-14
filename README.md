# Priority_based_Multithreaded_Image_Processing_Server

The goal of the project is to develop an image processing server that interacts with clients through a pool of worker threads using the producer consumer model.  
The server consists of a main thread and a set of worker threads withthe  main  thread  running  at  a  higher  priority  than  the  worker  threads.   
The main thread repeatedly accepts connection requests from clients and places theresulting connected descriptors in a bounded buffer.  
Each worker thread repeat-edly removes a descriptor from the buffer,  services the client,  and then waits for  the  next  descriptor.   
All  the  threads  are  scheduled  with  the  FIFO  policy.The  image  server  applies  image  processing  operations  on  the  image  input  bythe client.  
These image processing operations are derived from the open source OpenCV library.
