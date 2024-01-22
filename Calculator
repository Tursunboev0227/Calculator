import sys
from PyQt5.QtWidgets import(
    QApplication,
    QWidget,
    QPushButton,
    QLineEdit,
    QVBoxLayout,
    QHBoxLayout
)

class BlackButton(QPushButton):
    
    def __init__(self,text):
        super().__init__(text)
        self.setFixedSize(100,50)
        self.setStyleSheet("color : 'black'; border-radius : 18px;font-size: 20px;background : silver")

class Window(QWidget):

    def __init__(self) -> None:
        super().__init__()

        self.setFixedSize(500,300)
        self.setWindowTitle("Calculator")
        self.setStyleSheet('background : gold')
       
        self.edit = QLineEdit(self)
        self.edit.setFixedSize(336,50)
        self.edit.setStyleSheet("border-radius : 20px;background : white;font-weight: 500; color: black; font-size:12pt")

        self.clear = BlackButton('Clear')

        self.v_box = QVBoxLayout()
        self.h1_box = QHBoxLayout() 
        self.h2_box = QHBoxLayout() 
        self.h3_box = QHBoxLayout() 
        self.h4_box = QHBoxLayout() 
        self.h5_box = QHBoxLayout() 

        self.h5_box.addWidget(self.edit)
        self.h5_box.addWidget(self.clear)

        self.btn1 = BlackButton('1')
        self.btn2 = BlackButton('2')
        self.btn3 = BlackButton('3')
        self.btn4 = BlackButton('4')
        self.btn5 = BlackButton('5')
        self.btn6 = BlackButton('6')
        self.btn7 = BlackButton('7')
        self.btn8 = BlackButton('8')
        self.btn9 = BlackButton('9')
        self.btn10 = BlackButton('/')
        self.btn11 = BlackButton('*')
        self.btn12 = BlackButton('-')
        self.btn13 = BlackButton('+')
        self.btn14 = BlackButton('0')
        self.btn16 = BlackButton('.')

        self.h1_box.addWidget(self.btn1)
        self.h1_box.addWidget(self.btn2)
        self.h1_box.addWidget(self.btn3)
        self.h1_box.addWidget(self.btn10)

        self.h2_box.addWidget(self.btn4)
        self.h2_box.addWidget(self.btn5)
        self.h2_box.addWidget(self.btn6)
        self.h2_box.addWidget(self.btn11)

        self.h3_box.addWidget(self.btn7)
        self.h3_box.addWidget(self.btn8)
        self.h3_box.addWidget(self.btn9)
        self.h3_box.addWidget(self.btn12)

        win = QWidget()
        win.setFixedSize(40,30)
        self.btn15 = QPushButton(win)
        self.btn15.setText('=')
        self.btn15.setStyleSheet("background : 'red'; border-radius : 15px")
        self.btn15.setFixedSize(100,50)
        
        self.h4_box.addWidget(self.btn14)
        self.h4_box.addWidget(self.btn13)
        self.h4_box.addWidget(self.btn16)
        self.h4_box.addWidget(self.btn15)

        self.v_box.addLayout(self.h5_box)
        self.v_box.addLayout(self.h1_box)
        self.v_box.addLayout(self.h2_box)
        self.v_box.addLayout(self.h3_box)
        self.v_box.addLayout(self.h4_box)

        self.setLayout(self.v_box)

        self.btn1.clicked.connect(self.on1)
        self.btn2.clicked.connect(self.on2)
        self.btn3.clicked.connect(self.on3)
        self.btn4.clicked.connect(self.on4)
        self.btn5.clicked.connect(self.on5)
        self.btn6.clicked.connect(self.on6)
        self.btn7.clicked.connect(self.on7)
        self.btn8.clicked.connect(self.on8)
        self.btn9.clicked.connect(self.on9)
        self.btn10.clicked.connect(self.on10)
        self.btn11.clicked.connect(self.on11)
        self.btn12.clicked.connect(self.on12)
        self.btn13.clicked.connect(self.on13)
        self.btn14.clicked.connect(self.on14)
        self.btn15.clicked.connect(self.on15)
        self.btn16.clicked.connect(self.on16)
        self.clear.clicked.connect(self.on_clear)

        self.text = ''
    
    def  on_clear(self):
        
        self.edit.setText('')
        self.text = ''


    def on1(self):
        self.edit.setText('1')
        self.text += self.edit.text()
    
    def on2(self):
        self.edit.setText('2')
        self.text += self.edit.text()
    
    def on3(self):
        self.edit.setText('3')
        self.text += self.edit.text()
    def on4(self):
        self.edit.setText('4')
        self.text += self.edit.text()
    def on5(self):
        self.edit.setText('5')
        self.text += self.edit.text()
    
    def on6(self):
        self.edit.setText('6')
        self.text += self.edit.text()

    def on7(self):
        self.edit.setText('7')
        self.text += self.edit.text()

    def on8(self):
        self.edit.setText('8')
        self.text += self.edit.text() 

    def on9(self):
        self.edit.setText('9')
        self.text += self.edit.text()                               

    def on10(self):
        self.edit.setText('/')
        self.text += self.edit.text()

    def on11(self):
        self.edit.setText('*')
        self.text += self.edit.text()
    def on12(self):
        self.edit.setText('-')
        self.text += self.edit.text()
    def on13(self):
        self.edit.setText('+')
        self.text += self.edit.text()
    
    def on14(self):
        self.edit.setText('0')
        self.text += self.edit.text() 
    def on16(self):
        self.edit.setText('.')
        self.text += self.edit.text() 

    def on15(self):
        self.edit.setText(str(eval(self.text)))
    
app =QApplication(sys.argv)

win = Window()
win.show()
app.exec_()
