# 60-dyas-of-data-science
every day i ll be sharing information about data science form scratch


name=[]
cell_number=[]
cards_valid=[]
user=0
while user<=4:
    card_number=str(input("Enter your card number \n"))
    if (len(card_number)==14 or len(card_number)==16):
        month=int(input("Enter the month \n"))
        year=int(input("Enter the year \n"))
    else:
        print("invalid, enter again \n")
        continue
        
    if (month>=1 and month<=12) and year>=2020:
            cards_valid.append(card_number)
            user=user+1
            my_name=str(input("Enter your name \n"))
            name.append(my_name)
            my_number=int(input("Enter your mobile number \n"))
            cell_number.append(my_number)
    else:
        print("invalid card \n")
        continue
            

        

from random import randint
my_cvv=[randint(100,999),randint(100,999),randint(100,999),randint(100,999),randint(100,999)]
print(my_cvv)

cell_cvv={cell_number[i]:my_cvv[i] for i in range(len(cell_number))}
print(cell_cvv)

my_bank_dic={cards_valid[i]:{cell_number[i]:name[i]} for i in range(len(cards_valid))}
print(my_bank_dic)
