# Data-Structure-2020
## Week 1 (3/10) - Review of C++
  1. pointer
  2. class
  3. overloading
 
## Week 2 (3/17)
  1. c++ sting
  2. file I/O
  3. header files

## Week 3 (3/24) - Inheritance(繼承) & Polymorphism (多型)
  1. Inheritance
      * three main functionalities of OOP - Inheritance , Polymorphism , Encapsulation
      * create new class from exisiting class
  2. Polymorphism
      * binding - early / late binding
      * virtual function

## Week 4 (3/31) - Templates & Exception Handling
  1. Templates : generic programming
      * template <typename T>
  2. Vector
      * push_back()從後面加上一個數字
      * pop_back() 從後面刪掉一個數字
  3. Exception Handling
      * try and catch -> try 抓到錯誤就丟給catch 可以cout 來檢查是否有錯誤 
      * throw (logic_error e ) -> catch(logic_error e) cout  << e.what()
      * noexecpt; -> for functions that does not generate error
  
## Week 5 (4/7) - Arrays and linked-base bags
  1. Abstract data types
      * OOA,OOD and OOP
      * operation contracts - documentation
      * ADT bag
  2. Array based implementation
      * static-array
      * dynamic-array
  3. Linked-base Array
      * Node
      * Member function
      * Constructor & destructor
## Week 6 (4/14) - Recursion & Algorithm Efficiency
  1. Recursion
      * Basic concpets
        * Binary search
        * Factorial(階層)and Maximum
        * choosing k out of n g(n,k)->  base trace = g(k,k) or g(n,0)
      * Number of recursive  
        * Recursion vs Iteration
  2. Alogorithm
      * the knapsack problem
        * dynamic programing algorithm
      * the maximimflow problem
        * residual networks

## Week 7 (4/21)- Stacks
  1. Intro
  2. Application of stack
      * calculator
      * graph search 
      * recursion
  3. Implementation of stack
    
## Week 8 (5/5) - Lists
  1. The ADT lists opertations
      * empty
      * get the number
      * insert
      * remove
      * remove all
      * get(position) - look at the entry at a specific position
      * setEntry(position , newEntry) - replace an entry at a specific position
  2. Lists implementation
      * array-based list (different from array , list is not fixed size)
      * linked-list
        * assert:作用是現計算表示式 expression ，如果其值為假（即為0），那麼它先向stderr列印一條出錯資訊，然後通過呼叫 abort 來終止程式執行。
  3. Sorted list & implementation
  
## Week 9 (5/12) - Queues
  1. Queues and Priority queues
      * the ADT queue - first in first out
          * isEmpty(): see whether queue is empty
          * enqueue(newEntry): 將 newEntry 加到最後一個
          * dequeue(): 將第一個移除
          * peekFront(): return the first position
      * recognizing palindromes(回文)
          * stack + queue
      * ADT proiortuy queue
          * each item is associated with a proiority
      
  2. Application
      *
