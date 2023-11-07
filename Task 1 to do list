from tkinter import *
from tkinter import messagebox


def newTask():
    task = my_entry.get()
    if task != "":
        lb.insert(END, task)
        my_entry.delete(0, "end")
    else:
        messagebox.showwarning("warning", "Please enter some task.")


def deleteTask():
    lb.delete(ANCHOR)


s = Tk()
s.geometry('500x450+500+200')
s.title('to do list')
s.config(bg='grey')
s.resizable(width=False, height=False)
frame = Frame(s)
frame.pack(pady=10)
lb = Listbox(
    frame,
    width=25,
    height=8,
    font=('Times', 18),
    bd=0,
    fg='grey',
    highlightthickness=0,
    selectbackground='black',
    activestyle="none",
)
lb.pack(side=LEFT, fill=BOTH)
task_list = [
    'Drink water',
    'Eat breakfast',
    'go gym',
    'write software',
    'presentation time',
    'take a break',
    'read books',
    'paint canvas'
]
for item in task_list:
    lb.insert(END, item)
sb = Scrollbar(frame)
sb.pack(side=RIGHT, fill=BOTH)
lb.config(yscrollcommand=sb.set)
sb.config(command=lb.yview)
my_entry = Entry(
    s,
    font=('times', 24)
)

my_entry.pack(pady=20)
button_frame = Frame(s)
button_frame.pack(pady=20)
addTask_btn = Button(
    button_frame,
    text='Add Task',
    font='times 14',
    bg='green',
    padx=20,
    pady=10,
    command=newTask
)
addTask_btn.pack(fill=BOTH, expand=True, side=LEFT)
delTask_btn = Button(
    button_frame,
    text='Delete Task',
    font='times 14',
    bg='red',
    padx=20,
    pady=10,
    command=deleteTask
)
delTask_btn.pack(fill=BOTH, expand=True, side=LEFT)
s.mainloop()
