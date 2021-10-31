import java.util.*;
import java.awt.*;
import javax.swing.*;
import java.awt.event.*;

public class GUI09 extends JFrame implements ActionListener
{
    // Step 1 : create JLabel variable
    private JLabel label;
    private JButton button;
    private JButton button2;
    boolean on = true;
    // constructor
    public GUI09()
    {   
        // Step 2 : create JLabel object and store its reference in label
        label = new JLabel("Computers Are Fun");
        
        // Step 3 : set label attributes
        label.setLocation(10,  200);
        label.setSize( 450, 50);
        label.setForeground(Color.BLACK);
        label.setFont(new Font("Arial", Font.PLAIN, 48));
        
        // Step 4: add label to content pane of frame
        getContentPane().add(label);
        
        // set frame attributes
        setLayout(null);                                 
        setSize(500, 500);                              
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);  
        getContentPane().setBackground(Color.white);
        setVisible(true);
        button = new JButton("on");
        button2 = new JButton("off");
        // set button attributes
        button.setLocation(120,50);
        button.setSize(100, 50);
        button2.setLocation(270 ,50);
        button2.setSize(100, 50);
        // add button to frame
        getContentPane().add(button);
        getContentPane().add(button2);
        // Step 2: register listener with button
        button.addActionListener(this);
        button2.addActionListener(this);  
        // set frame attributes
        setLayout(null);
        setSize(500, 500);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);  
        button.setVisible(true);
        button2.setVisible(true);
    }
    
    
    public void actionPerformed(ActionEvent event)
    {
        if(event.getSource() == button)             // identify source
        {
            label.setVisible(true);
        }
        if(event.getSource() == button2)             // identify source
        {
            label.setVisible(false);
        }
    }
    
    // main method
    public static void main(String[] args)
    {
        GUI09 app = new GUI09();   // run program
    }
}  
