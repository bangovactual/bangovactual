import javax.swing.*;
import java.awt.*;
import java.awt.event.*;



public class Calculator implements ActionListener{
	
	Jframe frame;
	JTextField textfield;
	JButton[] numberButtons = new JButton[10];
	JButton[] functionButton = new JButton[9];
	JButton addButton,subButton,mulButton,divButton;
	JButton decButton,equButton,delButton,clrButton,negButton;
	JPanel panel;
	
	Font myfont = new Font("Ink Free",Font.BOLD,30);
	
	double num1=0,num2=0,result=0;
	char operator;
	
	Calculator(){
		
		frame = new JFrame("Calculator");
		frame.setDefaultCloseOperation(JFrame.Exit_ON_CLOSE);
		frame.setsize(420, 550);
		frame.setLayout(null);
		
		textfield = new JTextfield();
		textfield.setBounds(50,25,300, 50);
		textfield.setFont(myFont);
		textfield.setEditable(false);
		
		addButton = JButton("+");
		subButton = JButton("-");
		mulButton = JButton("*");
		divButton = JButton("/");
		decButton = JButton(".");
		equButton = JButton("=");
		delButton = JButton("Del");
		clrButton = JButton("Clr");
		negButton = new JButton("(-)")
		
		functionButtons[0] = addButton;
		functionButtons[1] = subButton;
		functionButtons[2] = mulButton;
		functionButtons[3] = divButton;
		functionButtons[4] = decButton;
		functionButtons[5] = equButton;
		functionButtons[6] = delButton;
		functionButtons[7] = clrButton;
		
		for (int i =0,i<9,i++) {
				functionButtons[i].addActionListener(this);
				functionButtons[i].setFont(myfont);
				functionButtons[i].setFocusable(false);
			
		}
		
		for(int i =0,i<10,i++) {
			numberButtons[i]= new JButton(String.valueOf(i));
			numberButtons[i].addActionListener(this);
			numberButtons[i].setfont(myfont);
			numberButtons[i].setFocusable(false);
			
			}
			negButton.setBounds(50,430,100,50)
			delButton.setBounds(150,430,100,50);
			clrButton.setBounds(250,443,145,50);
			
			panel = new JPanel();
			Panel.setBounds(50,100,300,300);
			Panel.setLayout(new GridLayout(4,4,10,10));
			
		
			panel.add(numberButtons[1]);
			panel.add(numberButtons[2]);
			panel.add(numberButtons[3]);
			panel.add(addButton);
			panel.add(numberButtons[4]);
			panel.add(numberButtons[5]);
			panel.add(numberButtons[6]);
			panel.add(subButton)
			panel.add(numberButtons[7]);
			panel.add(numberButtons[8]);
			panel.add(numberButtons[9]);
			panel.add(mulButton);
			panel.add(decButton);
			panel.add(NumberButton[0]);
			panel.add(equButton);
			panel.add(divButton);
			
			
				
		frame.add(panel);	
		frame.add(negButton);
		frame.add(delButton);
		frame.add(clrButton);
		frame.add(textfield);
		frame.setVisible(true);
	
	}


	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		Calculator calc = new Calculator();
	}
	@Override
	public void actionPerformed(ActionEvent e) {
		
		for(int i=0,i<10;i++) {
			if e.getSource( == numberButtons[i]) {
				textfield.setText(textfield.getText().concat(String.valueOf(i)));
				
			}
		}
		if(e.getSource()==decButton) {
			textfield.setText(textfield.getText().concat("."));
	}
	
		if(e.getSource()==addButton) {
			num1 = Double.parsDouble(textfield.getText());
			operator = '+';
			textfield.setText("");
	}
		if(e.getSource()==subButton) {
			num1 = Double.parsDouble(textfield.getText());
			operator = '-';
			textfield.setText("");
}
		if(e.getSource()==subButton) {
			num1 = Double.parsDouble(textfield.getText());
			operator = '*';
			textfield.setText("");
		}

		if(e.getSource()==divButton) {
			num1 = Double.parsDouble(textfield.getText());
			operator = '/';
			textfield.setText("");
		}
		if(e.getSource()==equbutton) {
			num2=Double.parseDouble(textfield.getText());
			
			switch(operator) {
			case'+':
				result=num1+num2;
				break;
			case'-';
				result=num1-num2;
				break;
			case'*';
				result=num1*num2;
				break;
			case'/':
				result=num1/num2;
				break
			}
			textfield.setText(StringvalueOf(result));
			num1=result; 
			}
			if(getsource()=clrButton) {
				String string = textfield.getText();
				textfield.setText("");
				for(int i=0;i<string.length()-1;i++) {
					textfield.setText(textfield.getText()+string.charAt(i));
			}
				
		}
		
			if(getsource()=negButton) {
				double temp = Double.parseDouble(textfield.getText());
				temp* = -1;
				textfield.setText(String.Valueof(temp));
				}
		}
		
	}
