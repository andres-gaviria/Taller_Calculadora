package calculadora;

import java.awt.EventQueue;

import javax.swing.JFrame;

import javax.swing.JButton;

import javax.swing.JTextField;

import java.awt.Color;

import java.awt.event.ActionListener;

import java.awt.event.ActionEvent;

public class calculadora {

	private JFrame frame;
	private JTextField txtpantalla;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					calculadora window = new calculadora();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public calculadora() {
		initialize();
	}
	String numero1, operador, numero2;

	
	private String initialize() {
		frame = new JFrame();
		frame.getContentPane().setForeground(Color.CYAN);
		frame.setBounds(100, 100, 264, 255);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		JButton Num0 = new JButton("0");
		Num0.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"0");
			}
		});
		Num0.setBounds(10, 188, 49, 23);
		frame.getContentPane().add(Num0);
		
		JButton Igual = new JButton("=");
		Igual.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				String resultado;
				numero2 = txtpantalla.getText();
				
				if(!numero2.equals("")) {
					resultado = calculadora (numero1,numero2,operador);
					txtpantalla.setText(resultado);
				}
			}
			public String calculadora(String numero1, String numero2, String operador) {
				Double resultado = 0.0;
				String Respuesta;
				
				if(operador.equals("+")) {
					resultado=Double.parseDouble(numero1) + Double.parseDouble(numero2);
				}
				else if(operador.equals("-")) {
					resultado=Double.parseDouble(numero1) - Double.parseDouble(numero2);
				}
				else if(operador.equals("/")) {
					resultado=Double.parseDouble(numero1) / Double.parseDouble(numero2);
				}
				else if(operador.equals("*")) {
					resultado=Double.parseDouble(numero1) * Double.parseDouble(numero2);
				}
				Respuesta = resultado.toString();
				return Respuesta;
				
			}
			
				
				
		});
		
		Igual.setBounds(69, 188, 108, 23);
		frame.getContentPane().add(Igual);
		
		JButton Multi = new JButton("*");
		Multi.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				if(!txtpantalla.getText().equals("")) {
					numero1 = txtpantalla.getText();
					operador= "*";
					txtpantalla.setText("*");
				}
			}
		});
		Multi.setBounds(187, 188, 49, 23);
		frame.getContentPane().add(Multi);
		
		JButton Num1 = new JButton("1");
		Num1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"1");
			}
		});
		Num1.setBounds(10, 154, 49, 23);
		frame.getContentPane().add(Num1);
		
		JButton Num2 = new JButton("2");
		Num2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"2");
			}
		});
		Num2.setBounds(69, 154, 49, 23);
		frame.getContentPane().add(Num2);
		
		JButton Num3 = new JButton("3");
		Num3.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"3");
			}
		});
		Num3.setBounds(128, 154, 49, 23);
		frame.getContentPane().add(Num3);
		
		JButton Divi = new JButton("/");
		Divi.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				if(!txtpantalla.getText().equals("")) {
					numero1 = txtpantalla.getText();
					operador= "/";
					txtpantalla.setText("/");
				}
			}
		});
		Divi.setBounds(187, 154, 49, 23);
		frame.getContentPane().add(Divi);
		
		JButton Num4 = new JButton("4");
		Num4.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"4");
			}
		});
		Num4.setBounds(10, 120, 49, 23);
		frame.getContentPane().add(Num4);
		
		JButton Num5 = new JButton("5");
		Num5.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"5");
			}
		});
		Num5.setBounds(69, 120, 49, 23);
		frame.getContentPane().add(Num5);
		
		JButton Num6 = new JButton("6");
		Num6.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"6");
			}
		});
		Num6.setBounds(128, 120, 49, 23);
		frame.getContentPane().add(Num6);
		
		JButton Resta = new JButton("-");
		Resta.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				if(!txtpantalla.getText().equals("")) {
					numero1 = txtpantalla.getText();
					operador= "-";
					txtpantalla.setText("-");
				}
			}
		});
		Resta.setBounds(187, 120, 49, 23);
		frame.getContentPane().add(Resta);
		
		JButton Num7 = new JButton("7");
		Num7.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"7");
			}
		});
		Num7.setBounds(10, 86, 49, 23);
		frame.getContentPane().add(Num7);
		
		JButton Num8 = new JButton("8");
		Num8.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"8");
			}
		});
		Num8.setBounds(69, 86, 49, 23);
		frame.getContentPane().add(Num8);
		
		JButton Num9 = new JButton("9");
		Num9.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText(txtpantalla.getText()+"9");
			}
		});
		Num9.setBounds(128, 86, 49, 23);
		frame.getContentPane().add(Num9);
		
		JButton Suma = new JButton("+");
		Suma.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				if(!txtpantalla.getText().equals("")) {
					numero1 = txtpantalla.getText();
					operador= "+";
					txtpantalla.setText("+");
				}
			}
		});
		Suma.setBounds(187, 86, 49, 23);
		frame.getContentPane().add(Suma);
		
		txtpantalla = new JTextField();
		txtpantalla.setBounds(114, 44, 122, 31);
		frame.getContentPane().add(txtpantalla);
		txtpantalla.setColumns(10);
		
		JButton Limpiar = new JButton("LIMPIAR");
		Limpiar.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent arg0) {
				txtpantalla.setText("");
			}
		});
		Limpiar.setBounds(10, 44, 94, 33);
		frame.getContentPane().add(Limpiar);
		return numero1;
	}
}
