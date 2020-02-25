package group_project;

import java.io.*;
import java.util.*;

public class Group_project {
	
	static Scanner userInputString = new Scanner(System.in);
	static Scanner userInputChar = new Scanner(System.in);
	static Scanner userInputInteger = new Scanner(System.in);
	static Scanner userInputDouble = new Scanner(System.in);
	
	
	public static void appendFile(String line){ 
		
		
		try {																								
			PrintWriter myFile = new PrintWriter (new BufferedWriter (new FileWriter ("users.txt", true)));	
			myFile.println(line);																			
			myFile.close();																					
			
		} catch(IOException e) {																			
			System.out.print("There is an I/O problem!");
		}
	
	}
	

	public static void main(String[] args) {

		
		// voor elke string moet nog private! private final kan volgens mij alleen in de public class
		
		System.out.println("Welcome to Hotel Booking PFM!");
		System.out.println("Do you already have an account?");
		
		String userAnswer = userInputString.nextLine();	
		
		if (userAnswer.equals("yes")) {
			System.out.println("Please continue to user login.");
		}
		else if (userAnswer.equals("no")) {
			System.out.println("Create account");
			
			System.out.println("First name: ");
			String firstName = userInputString.nextLine();
			String firstNameLine = "First name:      " + firstName;
			appendFile(firstNameLine);
			
			System.out.println("Last name: ");
			String lastName = userInputString.nextLine();
			String lastNameLine = "Last name:       " + lastName;
			appendFile(lastNameLine);
			
			System.out.println("Gender (F = Female, M = Male, O = Other: ");
			String gender = userInputString.nextLine(); //misschien veranderen naar char?
			String genderLine = "Gender:          " + gender;
			appendFile(genderLine);
			
			System.out.println("Date of birth (data/month/year): "); 
			String dateOfBirth = userInputString.nextLine(); //of moet het int zijn ipv string? 
			String dateOfBirthLine = "Date of birth:   " + dateOfBirth;
			appendFile(dateOfBirthLine);
			
			System.out.println("Address (Streetname + number, City, Postal code: "); //of doen we elke van deze onderdelen van een address apart appenden?
			String address = userInputString.nextLine();
			String addressLine = "Address:         " + address;
			appendFile(addressLine);
			
			System.out.println("Email: ");
			String email = userInputString.nextLine();
			String emailLine = "Email:           " + email;
			appendFile(emailLine);
			
			System.out.println("Phone: ");
			String phone = userInputString.nextLine();
			String phoneLine = "Phone:           " + phone;
			appendFile(phoneLine);
			
			System.out.println("Username: ");
			final String username = userInputString.nextLine(); 
			String usernameLine = "Username:        " + username;
			appendFile(usernameLine);
			
			System.out.println("Password: ");
			final String password = userInputString.nextLine(); 
			String passwordLine = "Password:        " + password;
			appendFile(passwordLine);
			
			
		}
	
		
	}

	
