1)

An exception is not like an error 
Exceptions can be handled
exception does not give errors
there are 2 types of exception that are namely
1) Built in exception 
2) User defined exception 
Built in exception are like :
DivisionByZero Exceptiom
FileNotFound Exception
IndexNotFound Exception
KeyNotFound Exception etc.
User Difined Exceptions are the exception that a programmer does
whenever exception during run time,program runs even if ther is exception 

Difference between Exception and Error
    Exception                                     Error
1)  Exception can be handled                     Errors cannot be handled
2)  Exception occur during runtime               Errors occurs at compile time
3)  When ther is exception progam executes       When there is error program does not exceute


2)
When the Exceptions are not handled then we cannot get the right output from the program
i,e We get error in the program
for example :
lets take zero division error
a = int(input("Enter a value"))
b = int(input("Enter b value"))
print(a/b)

output: Enter a value 10
        Enter b value 0 
        ZeroDivisionError: division by zero
So it is necessary to handle the exception so that we can get right output and get rid of Errors

3)

The python statements used to catch and handle exceptions are 
1)try
2)finally
3)raise

try :
try except is used to handle the exception like ZeroDivisionError,FileNotFound ,IndexNotFound Exceptions
example  
        try : 
        x=int(input("Enter value of x"))
        print(x/0)
        except Exception as e:
        print(e)
finally:when we use finally keyword then in the output even if there are any exception then,
 also the message written in finally we get executed
        try : 
        x=int(input("Enter value of x"))
        print(x/0)
        except Exception as e:
        print(e)
        finally:
        print("I am Sameer")
raise:The raise keyword in Python is used to raise exceptions explicitly
        def validage(age):
    if age < 0:
        raise ValueError("Age cannot be negative.")
try:
    age = int(input("Enter your age: "))
    validage(age)
except ValueError as e:
    print(e)

4)

try and else: try and else is used to handle the the exceptions of the program exceptions like ValueError,DivisionByZero,FileNotFound etc..
Example :
        try : 
        x=int(input("Enter value of x"))
        y=int(input("Enter value of y"))
        res = x/y # Let us a y value as zero to show exception
        print(res)
        except Exception as e:
        print(e)
        else:
        print(res)
Finally:when we use finally keyword then in the output even if there are any exception then,
 also the message written in finally we get executed
finally keyword is used to print any message for sure in program
        try : 
        x=int(input("Enter value of x"))
        print(x/0)
        except Exception as e:
        print(e)
        finally:
        print("I am Sameer")
raise:The raise keyword in Python is used to raise exceptions 
        def validage(age):
    if age < 0:
        raise ValueError("Age cannot be negative.")
try:
    age = int(input("Enter your age: "))
    validage(age)
except ValueError as e:
    print(e)


5)Custom Exceptions in python are the exception which are defind by thr programmer
we need custom exceptions for
1.Readability
2.to organize
3.better communication
4.problem solving
example:

class validage(Exception):
	def__init__(self,msg):
   		self.msg = msg
	defvalidage(age):
		if age < 0:
        	raise validage("Age cannot be negative.")
		else:
		raise validage("Valid age") 
	try:
    	age = int(input("Enter your age: "))
    	validage(age)
	except ValueError as e:
    	print(e)





6)


class validage(Exception):
	def__init__(self,msg):
   		self.msg = msg
	defvalidage(age):
		if age < 0:
        	raise validage("Age cannot be negative.")
		else:
		raise validage("Valid age") 
	try:
    	age = int(input("Enter your age: "))
    	validage(age)
	except ValueError as e:
    	print(e)
