# Login-system*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package login;
import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import  javax.swing.JTextField;
import javax.swing.JLabel;


/**
 *
 * @author 110899
 */
public class Login {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
      
        
        
       JFrame loginform=new JFrame (" login ");
    
       JLabel username=new JLabel ("username");
       username.setLocation(20,40);
       username.setSize(50,25);
       JTextField textfield= new JTextField ();
       textfield.setColumns(25);
       textfield.setSize(50,25);
       loginform.add(username);
       JLabel password=new JLabel ("password");
       password.setLocation(30,40);
       JTextField textfield2=new JTextField ();
       textfield.setColumns(25);
       textfield2.setSize(50,25);
       loginform.add(password);
       loginform.add(textfield2);
       
      
        JButton loginButton=new JButton ();
        loginButton.setText("login");
        loginButton.setToolTipText("this is the login button");
        loginButton.setSize(50,25);
        
        JButton button2=new JButton ("add user");
        button2.setToolTipText("this is the add user button");
        button2.setSize(50,25);
        
        loginform.add(loginButton);
        loginform.add(button2);
        
        JPanel panel=new JPanel();
        panel.add(loginButton);
        panel.add(button2);
        
        loginform.setSize(500,250);
        loginform.setLocationRelativeTo(null);
        loginform.add(panel);
    
        loginform.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        loginform.setVisible(true);
        
  {    
package login;
import java.awt.Color;
import javax.swing.*;


public class adduserImpl extends adduser {
    JFrame myframe=new JFrame("add user");
    JPanel mypanel=new JPanel();
    JLabel namelabel=new JLabel ("Name");
    JTextField name=new JTextField();
    
    JLabel genderlabel=new JLabel ("Gender");
    JTextField gender=new JTextField();
 
    JLabel telephonelabel=new JLabel ("Telephone Number");
    JTextField telephone=new JTextField();
    
    JLabel dateofbirthlabel=new JLabel ("Date of Birth");
    JTextField dateofbirth=new JTextField();
  
    JLabel agelabel=new JLabel ("Age");
    JTextField age=new JTextField();
    myframe.setVisible(true}
   
   
   import java.sql.Statement;
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
/**
 *
 * @author 110899
 */
public class database {
    public static void main(String[]args){
        try { 
            Connection conn=DriverManager.getConnection("jdbc:derby://localhost:1527/sample [app on APP]");
                    System.out.println("Connection Established");
                    Statement st=conn.createStatement();
                    ResultSet rs=st.executeQuery("Select * from  user");
                            while(rs.next())
                            {
                                System.out.print(rs.getString(1));
                                System.out.print(rs.getString(2));
                                System.out.print(rs.getString(3));
                                System.out.print(rs.getString(4));                           

                            }      
        } catch(Exception e){
                            
                            
                            System.out.print("Error");
                            }
            
        }
    }
    
    


  

