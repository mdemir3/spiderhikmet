# spiderhikmet
//there is life  there is hope

	/*  
	Hikmet Demir
	Programming Fundamentals 1
	COSC 13362001
	January 24, 2017
	A small company wants you to develop a small application to keep customers 
	informed when trying to purchase a new car.
	*/
package paymentssss;
import java.text.NumberFormat;
import java.util.Scanner;
public class Demirhomework {



	

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		double price;
		int months;
		double rate;
		
		Scanner keyboard = new Scanner(System.in);
		//Declaring to our scanner named by keyboard
		System.out.println("How much does it cost this vehicle?");
		//print statement for asking car price
		price = keyboard.nextInt();
		//getting car price from the user
		System.out.println(" The length of loan is in months :  ?");
	    //print statement for asking length of the loan
		months = keyboard.nextInt();
		//getting length of the loan from the user
		 System.out.print("The estimated percentage interest rate: " + "\n"
	                +"(Please enter your rate between 1 and 100) : ");
	        //Print statement for rate
		 rate = keyboard.nextDouble();
		 //getting the rate from the user
	        rate=rate/100;
	        //We got the rate as an integer for the calculation so we need to
	        //convert the number to double for calculation
	        //For the calculation I seperated the calculation in 2 pieces
	        double p1 = price * (rate/12);
	        //top side of the calculation
	        double p2 = 1- Math.pow((1+(rate/12)),(0-months));
	        //bottom side of the calculation
	        double payments = p1/p2;
	        //final division
	        
	        NumberFormat money = NumberFormat.getCurrencyInstance();
	        //creating a number format for the dollar sign and 2 decimal places
	        
	        System.out.println("Your payment is :  "+ money.format(payments));
	        //final answer
	        }

	}
