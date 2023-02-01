from tkinter import *
from tkinter import messagebox
import speech_recognition as sr
import pyttsx3
import time

san = "listening..."

r = sr.Recognizer()
engine = pyttsx3.init()

obj = pyttsx3.init()
obj.setProperty("rate",150)
obj.say("M.I.T.COLLEGE BOT")

app = Tk()


app.geometry("300x350")
app.title("M.I.T.COLLEGE BOT")

def save_msg():
	l2 = Label(app, text='LISTENING....', font="20")
	l2.place(x=10, y=10)
	time.sleep(1)
	run_b()

def run_b():
	run_bot()
	return ()

def talk(text):
	engine.say(text)
	engine.runAndWait()


def take_command():
	try:
		with sr.Microphone() as source:
			print('listening')
			voice  = r.listen(source)
			com  = r.recognize_google(voice)

			com = com.lower()
			if 'hey' in com:
				print(com)



	except:
		pass
	return com

def  run_bot():
	com = take_command()
	print(com)

	if 'college time' in com:
		print('college time is 9 a m to 5 p m ')
		talk('college time is 9 a. m .to 5 p. m. ')
		l2 = Label(app, text='9 a.m. to 5 p.m.                   ', font="30")
		l2.place(x=10, y=10)

	if 'contact' in com:
		print('you can contact on this number 7875112288')
		talk('you can contact on this number 7875112288')
		l2 = Label(app, text='contact: 7875112288                  ', font="30")
		l2.place(x=10, y=10)


	if 'location' in com:
		print('this places at satara by pass road')
		talk('this places at satara by pass road')
		l2 = Label(app, text='satara by pass road                    ', font="30")
		l2.place(x=10, y=10)

	if 'principal' in com:
		print('currently MR. awdute sir is principal')
		talk('currently mister awdute sir is principal')
		l2 = Label(app, text='MR. awdute sir                          ', font="30")
		l2.place(x=10, y=10)

	if 'branch' in com:
		print('electronics, computer, mechnical, and automobile')
		talk('electronics, computer, mechnical, and automobile')
		l2 = Label(app, text='ece, ccse, mec, and aum                 ', font="30")
		l2.place(x=10, y=10)

	if 'college fees' in com:
		print('per year 1 lac ')
		talk('per year 1 lac ')
		l2 = Label(app, text='per year 1 lac                        ', font="30")
		l2.place(x=10, y=10)

	if 'deposit' in com:
		print('deposite is 2 lac ')
		talk('deposite is 2 lac ')
		l2 = Label(app, text='depoisit 2 lac                    ', font="30")
		l2.place(x=10, y=10)

	if 'uniform' in com:
		print('sky blue shirt blue pant')
		talk('sky blue shirt blue pant')
		l2 = Label(app, text='sky blue shirt blue pant          ', font="30")
		l2.place(x=10, y=10)

	if 'canteen' in com:
		print('pure veg with 20 menu')
		talk('pure veg with 20 menu')
		l2 = Label(app, text='pure veg with 20 menu          ', font="30")
		l2.place(x=10, y=10)

	if 'library' in com:
		print('library with 2000 books')
		talk('library with 2000 books')
		l2 = Label(app, text='library with 2000 books          ', font="30")
		l2.place(x=10, y=10)

	if 'command' in com:
		l2 = Label(app, text='COLLEGE TIME', font="30")
		l2.place(x=10, y=10)
		l2 = Label(app, text='LOCATION', font="30")
		l2.place(x=10, y=30)
		l2 = Label(app, text='PRINCIPAL', font="30")
		l2.place(x=10, y=50)
		l2 = Label(app, text='CONTACT', font="30")
		l2.place(x=10, y=70)
		l2 = Label(app, text='BRANCH', font="30")
		l2.place(x=10, y=90)
		l2 = Label(app, text='FEES', font="30")
		l2.place(x=10, y=110)
		l2 = Label(app, text='DEPOSIT', font="30")
		l2.place(x=10, y=130)
		l2 = Label(app, text='UNIFORM', font="30")
		l2.place(x=10, y=150)
		l2 = Label(app, text='CANTEEN', font="30")
		l2.place(x=10, y=170)
		l2 = Label(app, text='LIBRARY', font="30")
		l2.place(x=10, y=190)

	if 'clear chat bot' in com:

		l2 = Label(app, text='                                    ', font="30")
		l2.place(x=10, y=10)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=30)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=50)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=70)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=90)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=110)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=130)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=150)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=170)
		l2 = Label(app, text='                         ', font="30")
		l2.place(x=10, y=190)

if __name__ == '__main__':


	button1 = Button(app, text="TALK", fg="white", font=('arial', 15, 'bold'), command=save_msg, width="15",
					 height="1", bg="black")
	button1.place(x=40, y=300)

	l2 = Label(app, text=san, font="20")
	l2.place(x=10, y=10)

	mainloop()





