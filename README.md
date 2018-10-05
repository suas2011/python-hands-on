# python-hands-on
This Program is written for new learners in Python 3.6.5, seeking the basics and menu/sub-menus controls with loops and simple statements including arithmetic operators, words input, and numbers input. They will also find suitable for event based loops and other Math related operations.


# making a user input based program

a=0
b=0
c=0
ch=0
operator=""
forwardreversetable=""

t=0
s=0
sqc=0
sqi=0   #square value for integer
sqf=0.0 #square value for float
f=0.0
import sys

while True:
    print()
    print("1-Calculator")
    print("2-Table")
    print("3-Squares Roots")
    print("4-Cube Roots")
    print("5-Quads")
    print("6-Exit")
    print()
    ch=int(input("enter your choice: "))

    if ch==1:
        print("you selected 1: Now Using Calculator ")
        print("+ Addition")
        print("- Subtraction")
        print("* Multiplication")
        print("/ Division")
        
        operator=str(input("enter arithmetic operator from the menu above:")) 

        if operator=="+":
                print("\nAddition")
                a=int(input("enter value of A: "))
                b=int(input("enter value of B: "))            
                c=a+b
                print("\nResult is: ",c)
        elif operator=="-":
                print("\nSubtraction")
                a=int(input("enter value of A: "))
                b=int(input("enter value of B: "))            
                c=a-b
                print("\nResult is: ",c)
        elif operator=="*":
                print("\nMultiplication")
                a=int(input("enter value of A: "))
                b=int(input("enter value of B: "))            
                c=a*b
                print("\nResult is: ",c)
        elif operator=="/":
                print("\nDivision")
                a=int(input("enter value of A: "))
                b=int(input("enter value of B: "))            
                c=a/b
                print("\nResult is: ",c)
        else:
            print("Sorry! invalid Operator entered!")
        
    elif ch==2:
        print("you selected 2, Construction of Tables!\n ")
        print("ForwardTable: Tables")
        print("ReverseTable: Tables")
        forwardreversetable=str(input("\nEnter the word 'ForwardTable' to generate Table in forword\n 'ReverseTable' to generate Table in reverse.\n"))

        if forwardreversetable=="forwardtable" or forwardreversetable=="ForwardTable" or forwardreversetable=="FORWARDTABLE":
            print("Forward Table Generation")
            t=int(input("enter table no:"))
            b=int(input("enter table beginning value/start value: "))
            s=int(input("enter table stop value: "))

            for count in range(b,s+1):
                c=t*count
                print(t,"=",count," * ",c)

        elif forwardreversetable=="reversetable" or forwardreversetable=="ReverseTable" or forwardreversetable=="REVERSETABLE":
            print("Reverse Table Generation")
            t=int(input("enter table no:"))
            b=int(input("enter table beginning value/start value: "))
            s=int(input("enter table stop value: "))

            for count in range(s,b-1,-1): #reverse counting
                c=t*count
                print(t,"=",count," * ",c)
        
        else:
            print("Invalid keyword entered!")

        
    elif ch==3:
        print("you selected 3, Generate Squares")
        print("1-Integer Square")
        print("2-Float Square")
        print("3-Integer Square Table")
        sqs=int(input("enter your option: "))
        if sqs==1:
            sqi=int(input("enter integer number: "))
            print(sqi*sqi)
        elif sqs==2:
            sqf=float(input("enter float number: "))
            print(sqf**2)
        elif sqs==3:
            sqit=int(input("enter integer range [1 to 20]: "))
            for a in range(1,sqit+1):
                print(a," |", a**2)
        else:
            print("invalid choice, enter correct choice!")
                  

            
    elif ch==4:
        print("you selected 4, Generate Cubes")
        print("1-Integer Cubes")
        print("2-Float Cubes")
        print("3-Integer Cubes Table")
        sqc=int(input("enter your option: "))
        if sqc==1:
            sqi=int(input("enter integer number: "))
            print(sqi**3)
        elif sqc==2:
            sqf=float(input("enter float number: "))
            print(sqf**3)
        elif sqc==3:
            sqit=int(input("enter integer range [1 to 20]: "))
            for a in range(1,sqit+1):
                print(a," |", a**3)
        else:
            print("invalid choice, enter correct choice!")
    elif ch==5:
        print("you selected 5, Generate Quads")
        print("1-Integer Quad")
        print("2-Float Quad")
        print("3-Integer Quad Table")
        sqq=int(input("enter your option: "))
        if sqq==1:
            sqi=int(input("enter integer number: "))
            print(sqi**4)
        elif sqq==2:
            sqf=float(input("enter float number: "))
            print(sqf**4)
        elif sqq==3:
            sqit=int(input("enter integer range [1 to 20]: "))
            for a in range(1,sqit+1):
                print(a," |", a**4)
        else:
            print("invalid choice, enter correct choice!")
    elif ch==6:
        print("you selected 6 Now Exits the program, Thanks for using the program!")
        sys.exit()
    else:
        print("you entered invalid choice!")
    
