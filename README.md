# css407hw3
Systems II Homework 3

Derek Krebs
Due: March 8, 2018


Thread programming (50 Points)

main() should:
  Create 2 child threads, both that run evaluate(). The evaluate() function should be passed the address of nodeBuffer.
  Run makeNode() NUM_PROBLEMS times, and put the returned node address in nodeBuffer.
  Wait for both child threads to finish
  
evaluate() should NUM_PROBLEM/2 times do:
  Save the value returned by the pullOut() method into a Node* variable.
  Print the iteration number, the node expression (obtainable as a C-string with the expression: nodePtr->toString().c_str()) and the value   the node evaluates to (nodePtr->eval()).
  delete the node pointer variable
  
After the loop, the function should just return(NULL).

Stop and try your program now. It is multi-threaded, but not thread-safe. It should not work properly.

Make NodeBuffer thread safe by giving it the necessary mutex(es) and condition(s). Where is/are the critical sections? Be sure to destroy your variables in ~NodeBuffer()!
