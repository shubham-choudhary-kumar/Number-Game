/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package swingproject;
import java.awt.GridLayout;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.io.File;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
import javax.swing.*;
public class Numbergame implements ActionListener
{
    String path="E:\\NetBeans IDE 8.2\\SwingProject\\src\\swingproject\\images\\";
  File file=new File("Numbergame.java");  
  JButton b1,b2,b3,b4,b5,b6,b7,b8,b9;
  //char c=92;
  JFrame frame;
  static ArrayList<String> arr=new ArrayList<String>();
  Numbergame()
  {
     // String path=file.getAbsolutePath();
      //path=path.substring(0,path.length()-15)+"\\ image \\";
      //path.replace("c+c","c");
      //System.out.println(path);
      frame=new JFrame("number game");
      frame.setSize(600,600);
      frame.setResizable(false);
      
       b1 = new JButton(new ImageIcon(path+arr.get(0)));
        b1.setText(arr.get(0).charAt(0)+"");
       
        b2 = new JButton(new ImageIcon(path+arr.get(1)));
        b2.setText(arr.get(1).charAt(0)+"");
       
        b3 = new JButton(new ImageIcon(path+arr.get(2)));
        b3.setText(arr.get(2).charAt(0)+"");

        b4 = new JButton(new ImageIcon(path+arr.get(3)));
        b4.setText(arr.get(3).charAt(0)+"");

        b5 = new JButton(new ImageIcon(path+arr.get(4)));
        b5.setText(arr.get(4).charAt(0)+"");

        b6 = new JButton(new ImageIcon(path+arr.get(5)));
        b6.setText(arr.get(5).charAt(0)+"");

        b7 = new JButton(new ImageIcon(path+arr.get(6)));
        b7.setText(arr.get(6).charAt(0)+"");

        b8 = new JButton(new ImageIcon(path+arr.get(7)));
        b8.setText(arr.get(7).charAt(0)+"");

        b9 = new JButton();
        b9.setText("");
      
      
      frame.add(b1);
      frame.add(b2);
      frame.add(b3);
      frame.add(b4);
      frame.add(b5);
      frame.add(b6);
      frame.add(b7);
      frame.add(b8);
      frame.add(b9);
        
      b1.addActionListener(this);
      b2.addActionListener(this);
      b3.addActionListener(this);
      b4.addActionListener(this);
      b5.addActionListener(this);
      b6.addActionListener(this);
      b7.addActionListener(this);
      b8.addActionListener(this);
      b9.addActionListener(this);
      
      
      frame.setLayout(new GridLayout(3,3));
      
      
      
     frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
     
     frame.setVisible(true);
  }
  public static void generateRandomPosition(){
       arr.add("1.jpg");
       arr.add("2.jpg");
       arr.add("3.jpg");
       arr.add("4.jpg");
       arr.add("5.jpg");
       arr.add("6.jpg");
       arr.add("7.jpg");
       arr.add("8.jpg");
       Collections.shuffle(arr);
   }
  public static void main(String ars[])
  {
      generateRandomPosition();
      new Numbergame();
  }

    @Override
    public void actionPerformed(ActionEvent e) 
    {
   
         //Button 1 Code
if(e.getSource()==b1){
if(b2.getText()==""){
b2.setIcon(new ImageIcon(path+b1.getText()+".jpg"));
b2.setText(b1.getText());
b1.setText("");
b1.setIcon(new ImageIcon(""));
}
else if(b4.getText()==""){
b4.setIcon(new ImageIcon(path+b1.getText()+".jpg"));
b4.setText(b1.getText());
b1.setText("");
b1.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//Button 2 Code
if(e.getSource()==b2){
if(b1.getText()==""){
b1.setIcon(new ImageIcon(path+b2.getText()+".jpg"));
b1.setText(b2.getText());
b2.setText("");
b2.setIcon(new ImageIcon(""));
}
else if(b3.getText()==""){
b3.setIcon(new ImageIcon(path+b2.getText()+".jpg"));
b3.setText(b2.getText());
b2.setText("");
b2.setIcon(new ImageIcon(""));
}
else if(b5.getText()==""){
b5.setIcon(new ImageIcon(path+b2.getText()+".jpg"));
b5.setText(b2.getText());
b2.setText("");
b2.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//Button 3 Code
if(e.getSource()==b3){
if(b2.getText()==""){
b2.setIcon(new ImageIcon(path+b3.getText()+".jpg"));
b2.setText(b3.getText());
b3.setText("");
b3.setIcon(new ImageIcon(""));
}
else if(b6.getText()==""){
b6.setIcon(new ImageIcon(path+b3.getText()+".jpg"));
b6.setText(b3.getText());
b3.setText("");
b3.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//Button 4 Code
if(e.getSource()==b4){
if(b1.getText()==""){
b1.setIcon(new ImageIcon(path+b4.getText()+".jpg"));
b1.setText(b4.getText());
b4.setText("");
b4.setIcon(new ImageIcon(""));
}
else if(b5.getText()==""){
b5.setIcon(new ImageIcon(path+b4.getText()+".jpg"));
b5.setText(b4.getText());
b4.setText("");
b4.setIcon(new ImageIcon(""));
}
else if(b7.getText()==""){
b7.setIcon(new ImageIcon(path+b4.getText()+".jpg"));
b7.setText(b4.getText());
b4.setText("");
b4.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//Button 5 code
if(e.getSource()==b5){
if(b2.getText()==""){
b2.setIcon(new ImageIcon(path+b5.getText()+".jpg"));
b2.setText(b5.getText());
b5.setText("");
b5.setIcon(new ImageIcon(""));
}
else if(b4.getText()==""){
b4.setIcon(new ImageIcon(path+b5.getText()+".jpg"));
b4.setText(b5.getText());
b5.setText("");
b5.setIcon(new ImageIcon(""));
}
else if(b6.getText()==""){
b6.setIcon(new ImageIcon(path+b5.getText()+".jpg"));
b6.setText(b5.getText());
b5.setText("");
b5.setIcon(new ImageIcon(""));
}
else if(b8.getText()==""){
b8.setIcon(new ImageIcon(path+b5.getText()+".jpg"));
b8.setText(b5.getText());
b5.setText("");
b5.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//Button 6 Code
if(e.getSource()==b6){
if(b3.getText()==""){
b3.setIcon(new ImageIcon(path+b6.getText()+".jpg"));
b3.setText(b6.getText());
b6.setText("");
b6.setIcon(new ImageIcon(""));
}
else if(b5.getText()==""){
b5.setIcon(new ImageIcon(path+b6.getText()+".jpg"));
b5.setText(b6.getText());
b6.setText("");
b6.setIcon(new ImageIcon("")); 
}
else if(b9.getText()==""){
b9.setIcon(new ImageIcon(path+b6.getText()+".jpg"));
b9.setText(b6.getText());
b6.setText("");
b6.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//Button 7 code
if(e.getSource()==b7){
if(b8.getText()==""){
b8.setIcon(new ImageIcon(path+b7.getText()+".jpg"));
b8.setText(b7.getText());
b7.setText("");
b7.setIcon(new ImageIcon(""));
}
else if(b4.getText()==""){
b4.setIcon(new ImageIcon(path+b7.getText()+".jpg"));
b4.setText(b7.getText());
b7.setText("");
b7.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//Button 8 code
if(e.getSource()==b8){
if(b5.getText()==""){
b5.setIcon(new ImageIcon(path+b8.getText()+".jpg"));
b5.setText(b8.getText());
b8.setText("");
b8.setIcon(new ImageIcon(""));
}
else if(b7.getText()==""){
b7.setIcon(new ImageIcon(path+b8.getText()+".jpg"));
b7.setText(b8.getText());
b8.setText("");
b8.setIcon(new ImageIcon(""));
}
else if(b9.getText()==""){
b9.setIcon(new ImageIcon(path+b8.getText()+".jpg"));
b9.setText(b8.getText());
b8.setText("");
b8.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//Button 9 Code
if(e.getSource()==b9){
if(b6.getText()==""){
b6.setIcon(new ImageIcon(path+b9.getText()+".jpg"));
b6.setText(b9.getText());
b9.setText("");
b9.setIcon(new ImageIcon(""));
}
else if(b8.getText()==""){
b8.setIcon(new ImageIcon(path+b9.getText()+".jpg"));
b8.setText(b9.getText());
b9.setText("");
b9.setIcon(new ImageIcon(""));
}
else{
JOptionPane.showMessageDialog(frame, "Inavid Selection Retry");
}
}

//code for wining
if(b1.getText().equals("1") && b2.getText().equals("2") && b3.getText().equals("3") && b4.getText().equals("4") && b5.getText().equals("5") && b6.getText().equals("6") && b7.getText().equals("7") && b8.getText().equals("8")){
            JOptionPane.showMessageDialog(frame, "Congratulations You Won.....");
        }

     }
    }
