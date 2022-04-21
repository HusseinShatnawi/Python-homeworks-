# Python-homeworks-
# Student name : Hussein Shatnawi
# CWID : 50305640
# HW1 / Q 2 
# This program is to enable the user inter some varaibles and these varaibles will be stored in a list
# Then if the user wants to swap the index of these variables then :
# The program will check the conditions; then it wil execute this swaping process 


# Firstly : We define the list as empety list, also we deifne a counter to count the trials 

list1= []
counter = 0

l = (input( " Please Enter a character : "))    # here we make input statment to enables the user to enter the varriables he wants
while l != 'x':                          # While loop to check the entered vairables are not the letter x
  list1.append(l)                        # the append function to add the entered varaibles to the list
  counter +=1                            # the counter will be increased for every input process
  l= input(' Please enter another charachter : ')
list1.append('x')                        # To add the loop ternimator condition ( x letter )
print( 'The number of trials is : ',counter+1)  # To show number of trials 
print(' Your list is : ',list1, ' and the length of the list is ', len(list1))  # To show the list we have 


swap = input(' write yes if you want to swap indeceis ! ')     # To ask the user if he wants swap the indeces 

while swap == 'yes' :


  swap1= int(input('Enter the index you want to exchange?'))        # input statement for the first index                                

  while swap1 >= len(list1) or swap1 < 0 :                          # To check the entered number 
    print(' You exceed the limit, please re-enter correct index')
    print(' NOTE : The max limit for you is : 0 -', len(list1) -1)   
    swap1= int(input(''))                                           # input statement in case the first trial was wrong 
 

  replacedBy = int(input(" Enter the index to be replaced by :"))   # input statement for the second index
  
  while replacedBy >= len(list1) or replacedBy < 0:                 # condition to make sure the entered number is not wrong
    print(' You exceed the limit, please re-enter correct index')
    print(' NOTE : The max limit for you is : 0 -', len(list1) -1)
    replacedBy= int(input(''))                                      # input statement to re_enter the second index
 


  swap1Index = list1[swap1]                                         # here we define an intermediate variable to store the value of first index which should be swapepd 
  replacedByIndex = list1[replacedBy]                               # here we define the second intermediate variable to store the value of second index which should be swapped 

  
  list1[swap1] = replacedByIndex                                    # here we assign the values for the indeceis as required 
  list1[replacedBy] = swap1Index                                    # same assigning process


  print(list1)                                                      # here to show the results 



  swap = input(' Do you want to swap more indecies  ?')            #  input statement to ask the user if he wants to swap more indecies 
            
  
  

print(' No swapping is needed ,  so your list is ')
print( list1)                                                      # Presenting the final results ( Final list shape ) 


