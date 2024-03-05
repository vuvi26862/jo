students_name = input("student's name")
def inputNumber(promt):
   noError = False
   while noError ==False:
     try:
       magicNumber = float(input(promt))
       return magicNumber
     except Exception:
        print("error")
def calculate_gpa():
   product = 0
   for i in range(0,len(subjects)):
       product += grades[i]*credits[i]
   return product / (sum(credits))
subjects = ["physical","chemistry",] #subject
credits = [] #credit
grades = []  #gardes
for subject in subjects:
 garde = inputNumber(f"enter point {subject}")
 grades.append(garde)
 credit = inputNumber(f"enter point {subject}")
 credits.append(credit)
print(calculate_gpa())
print(f"{students_name}'s GPA is: {calculate_gpa}")
with open('txt','w') as file:
      file.write(f'{students_name}, {credits}, {grades}, {calculate_gpa}')
