def markshet(marks):
    count=0
    mrksum=sum(marks)
    percent=round((mrksum/7),2)
    for i in marks:
        if i<40:
            count+=1
    else:
        if (count==1 or count==2 or count==3):
                x="You are Failed...!"
        elif count>3:
                x="You are Droped" 
        elif i>=40:
            print("Congratulation..")
            if percent<40:
                x=str(percent)+"% and got 'E' grade"
            elif percent>=40 and percent<50:
                x=str(percent)+"% and got 'D' grade"
            elif percent>=50 and percent<70:
                x=str(percent)+"% and got 'C' grade"
            elif percent>=70 and percent<80:
                x=str(percent)+"% and got 'B' grade"
            elif percent>=80 and percent<90:
                x=str(percent)+"% and got 'A' grade"
            else:
                x=str(percent)+"% and got 'O' grade" 
    return x       
marks=[]
for i in range(1,8):
    mk=int(input("Enter your marks: "))
    marks.append(mk)
print(markshet(marks))
