from tkinter import *
from tkinter import font as tkfont
from tkinter import messagebox

w=Tk()
w.geometry('350x500')
w.title(' L O G I N ')
w.resizable(0,0)


#Making gradient frame
j=0
r=10
for i in range(100):
    c=str(222222+r)
    Frame(w,width=10,height=500,bg="#"+c).place(x=j,y=0)   
    j=j+10                                                  
    r=r+1

Frame(w,width=250,height=400,bg='white').place(x=50,y=50)


usernameframe=Label(w,text='Username',bg='white')
font=('Consolas',13)
usernameframe.config(font=font)
usernameframe.place(x=80,y=200)

#usernameframe entry for username entry
usernameentry=Entry(w,width=20,border=0)
font=('Consolas',13)
usernameentry.config(font=font)
usernameentry.place(x=80,y=230)

#passwordentry entry for password entry
passwordentry=Entry(w,width=20,border=0,show='*')
passwordentry.config(font=font)
passwordentry.place(x=80,y=310)


l2=Label(w,text='Password',bg='white')
font=('Consolas',13)
l2.config(font=font)
l2.place(x=80,y=280)


###lineframe on entry

Frame(w,width=180,height=2,bg='#141414').place(x=80,y=332)
Frame(w,width=180,height=2,bg='#141414').place(x=80,y=252)





imagea=Image.open("D:\\TelU\\semester 2\\ALPRO\\TUBESSS\\xixixii\\login\\telu.jpg")
imageb= ImageTk.PhotoImage(imagea)

label1 = Label(image=imageb,
               border=0,
               
               justify=CENTER)


label1.place(x=115, y=50)


#Command
def cmd():
    if usernameentry.get()=='TelU company' and passwordentry.get()=='admin':
        messagebox.showinfo("LOGIN SUCCESSFULLY", "         W E L C O M E        ")
        w.destroy()
        
    else:
        messagebox.showwarning("LOGIN FAILED","        PLEASE TRY AGAIN        ")
        

#Button_with hover effect
def bttn(x,y,text,ecolor,lcolor):
    def on_entera(e):
        myButton1['background'] = ecolor #ffcc66
        myButton1['foreground']= lcolor  #000d33

    def on_leavea(e):
        myButton1['background'] = lcolor
        myButton1['foreground']= ecolor

    myButton1 = Button(w,text=text,
                   width=20,
                   height=2,
                   fg=ecolor,
                   border=0,
                   bg=lcolor,
                   activeforeground=lcolor,
                   activebackground=ecolor,
                       command=cmd)
                  
    myButton1.bind("<Enter>", on_entera)
    myButton1.bind("<Leave>", on_leavea)

    myButton1.place(x=x,y=y)


bttn(100,375,'L O G I N','white','#994422')


w.mainloop()

s = Tk()
s.title("TelU company")
s.resizable(width=False,height=False)

styling = tkfont.Font(family='Helvetica',weight='bold', size=15)
styling2 = tkfont.Font(family='Helvetica', size=9)


HEIGHT = 500
WIDTH = 600
canvas = Canvas(s, height=HEIGHT, width=WIDTH, bg='#000d33')
canvas.pack()


abjad = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
# fungsi enkripsi dengan parameter abjad
def enkripsi(abjad):  
    dt = Dataentry.get() 
    kt = int(keyEntry.get()) 

    result = ''
    for char in dt: 
        if char in abjad:  
            n = abjad.index(char)
            encrypt = (n - kt) % 26 
            convert = abjad[encrypt] 
            result = result + convert 
        else:
            result = result + ' ' 
    messagebox.showinfo("Enkripsi",result)

#fungsi dekripsi dengan parameter abjad
def deskripsi(abjad):
    dt = Dataentry.get()
    kt = int(keyEntry.get())

    result = '' 
    for char in dt: 
        if char in abjad:
            n = abjad.index(char) 
            encrypt = (n + kt) % 26 
            convert = abjad[encrypt] 
            result = result + convert 
        else:
            result = result + ' ' 
    messagebox.showinfo("Data",result)


frameJudul = Frame(s, bg='white')
frameJudul.place(rely=0.025,relx=0.5,relheight=0.1,relwidth=0.8,anchor='n')
judul = Label(frameJudul, bg='white', text='Enkripsi System (TelU Company)',font=styling)
judul.place(relheight=1,relwidth=1)

framedata = Frame(s, bg='white')
framedata.place(rely=0.2,relx=0.5,relheight=0.06,relwidth=0.8,anchor='n')
Datainfo = Label(framedata, bg='white', text='Data',font=styling2)
Datainfo.place(relwidth=0.4,relheight=1)
Dataentry = Entry(framedata)
Dataentry.place(relx=0.4,relheight=1,relwidth=0.6)


framekey = Frame(s, bg='white')
framekey.place(rely=0.27,relx=0.5,relheight=0.06,relwidth=0.8,anchor='n')
keyinfo = Label(framekey, bg='white', text='key', font=styling2)
keyinfo.place(relwidth=0.4,relheight=1)
keyEntry = Entry(framekey)
keyEntry.place(relx=0.4,relheight=1,relwidth=0.6)


frameButton = Frame(s, bg='white')
frameButton.place(rely=0.675,relx=0.5,relheight=0.3,relwidth=0.3,anchor='n')
Enkripsi = Button(frameButton,text='Enkripsi', command=lambda:enkripsi(abjad))
Enkripsi.place(rely=0,relx=0.5,relheight=0.25,relwidth=1, anchor='n')
Deskripsi = Button(frameButton,text='Deskripsi', command=lambda:deskripsi(abjad))
Deskripsi.place(rely=0.25,relx=0.5,relheight=0.25,relwidth=1, anchor='n' )
Exit = Button(frameButton, text='Exit', command=s.quit)
Exit.place(rely=0.5,relx=0.5,relheight=0.25,relwidth=1, anchor='n')

s.mainloop()
