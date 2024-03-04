# File_IO
Creating File and Taking Input from user


package com.edubridge;

import java.io.*;
import java.util.Scanner;

public class FileRW {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		
		
		
		
		
		try {
			File f=new File("C:/files/javid.txt");
			FileWriter fw=new FileWriter(f);
			BufferedWriter bw=new BufferedWriter(fw);
			System.out.println("Enter the First Line");
			bw.write(sc.nextLine()+"\n");
			System.out.println("Enter the Second Line");
			bw.write(sc.nextLine()+"\n");
			bw.flush();
			
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}

		 
		try {
			File f=new File("C:/files/javid.txt");
			FileReader fr = new FileReader(f);
			BufferedReader bf=new BufferedReader(fr);
			String data=bf.readLine();
			System.out.println(data);
			while(data!=null)
			{
			data = bf.readLine();
			System.out.println(data);
			}
			
		} catch (FileNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		
		
	}

}

