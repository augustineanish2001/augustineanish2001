- 👋 Hi, I’m @augustineanish2001
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
augustineanish2001/augustineanish2001 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
from tkinter import  *

def add():
    num1=number1.get()
    num2=number2.get()
    num3=number3.get()
    result=int(num1)*int(num2)*int(num3)
    labelresult.configure(text='result:%d'%result)

obj = Tk()
obj.geometry('500x600')
obj.title('operations')
obj.configure(bg='aqua')

Label(obj, text='enter value A:', font=('calibri', 15, 'bold'), bg='orange').grid(row=1, column=1)
Label(obj, text='enter value B:', font=('calibri', 15, 'bold'), bg='white').grid(row=2, column=1)
Label(obj, text='enter value C:', font=('calibri', 15, 'bold'), bg='green').grid(row=3, column=1)

number1 = StringVar()
number2 = StringVar()
number3 = StringVar()

Entry(obj, textvariable=number1, font=('calibri', 15)).grid(row=1, column=2)
Entry(obj, textvariable=number2, font=('calibri', 15)).grid(row=2, column=2)
Entry(obj, textvariable=number3, font=('calibri', 15)).grid(row=3, column=2)

Button(obj, text='submit',font=('calibri',15,'bold'),command=add,bg='gray',fg='white',width='10',height='1').grid(row=4,column=3)


labelresult=Label(obj,font=('calibri',15,'bold'),bg='aqua',fg='red')
labelresult.grid(row=5,column=3)

obj.mainloop()
