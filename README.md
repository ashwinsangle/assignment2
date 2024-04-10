# assignment2
//Find the Fibonacci Series up to Nth Term in Java Language
//a. Method 1: Using Iteration (Using Three variables)
//b. Method 2: Using Recursion
//c. Method 3: Using Formula a[i]=a[i-1]+a[i-2] (Using Array)

package assignment2;

public class Question1 {

		public static void main(String[] args) {
			int arr[],c;
			
			arr=new int[8];
			arr[0]=0;
			arr[1]=1;
			
			System.out.print(arr[0]+" "+arr[1]);
			for(int i=2;i<8;i++)
			{
				arr[i]=arr[i-1]+arr[i-2];
			   System.out.print(" "+ arr[i]);
						
			}

		}
  }


//Program to check Harshad number or not using Java
//Hint: - Harshad number is a number or an integer in base 10 which is
//completely divisible by sum of its digits.
//Example :
//Suppose a number 24 . Calculate the sum of digits of the number (2 +
//4) = 6 .
//Check whether the number entered by user is completely divisible by
//sum of its digits or not.
package assignment2;
import java.util.Scanner;
public class Harshad {

	public static void main(String[] args) {
		int n;
	     Scanner sc=new Scanner(System.in);
	     System.out.println("Enter the number");
	     n=sc.nextInt();
	     int temp=n;
	     int sum=0;

	     while(temp>0)
	     {
	    	 sum+=temp%10;
	    	 temp=temp/10;
	     }
	  
	     System.out.println(sum);
	   
		if(n%2==0)
		{
			System.out.println("divisible ");
		}
		else
		{
			System.out.println("not divisible");
		}
	}

}




package javaassignment2;

public class Factorial {

	private int num,fact=1;
	
	
	public Factorial(int num) {
		super();
		this.num = num;
		this.fact = fact;
	}
	
	public int display()
	{
		for(int i=1;i<=num;i++)
		{
			fact=fact*i;
		}
		return fact;
	}


	public static void main(String[] args) {
		Factorial f=new Factorial(5);
		System.out.println(F.display());
	}

}


//Java Program for Sorting first half in Ascending order and second half in
//Descending order
//Example
//Input : arr[6] = [1, 90, 34, 89, 7, 9]
//Output : 1 7 9 90 89 34
package assignment2;
//import java.sql.Array;
import java.util.Arrays;
public class Array {

	public static void main(String[] args) {
		int arr[]= {2,4,1,6,5,3},i;
		for(i=0;i<6;i++)
		{
			Arrays.sort(arr);
			int start=arr.length/2;
			int end=arr.length-1;
			while(start<end)
			{
				int temp=arr[start];
				arr[start]=arr[end];
				arr[end]=temp;
				start++;
				end--;
			}
			for(i=0;i<arr.length;i++)
			{
				System.out.print(" "+arr[i]);
			}
			
		}
	}

}


//Java program to count numbers of even and odd elements in an array

package javaassignment2;

public class Question5 {

	public static void main(String[] args) {
		int arr[]= {1,5,1,2,6,3};
		int Count1=0;
		int Count2=0;
		
		for(int i=0;i<6;i++)
		{
			if(arr[i]%2==0)
			{
				Count1++;
			}
			else {
				Count2++;
			}
		}
		System.out.println("Even Numbers : "+Count1);
		System.out.println("Odd Numbers : "+Count2);
	}

}

package javaassignment2;

public class Question6 {

	public static void main(String[] args) {
		int arr[] = {1,2,3,4,5};
        int n = arr.length;
        int k = 3;
        
        int[] temp;
         
        temp =  new int[n];
        
        for(int i=0;i<5;i++)
        {
        	System.out.print(arr[i] +" ");
        }
        
        System.out.println();
        
        for(int i=0; i<k; i++)
            temp[i] = arr[i];
    
        int x = k;
        for(int i=0; x < n; i++)
        {
            arr[i] = arr[x++];
        }
        
        x = 0;
    
        for(int i=n-k; i<n; i++)
            arr[i] = temp[x++];
    
   
        for (int i = 0; i < 7; i++)
            System.out.print(arr[i] + " ");
    }
    }

    package javaassignment2;

public class Question7 {

	public static void main(String[] args) {
		int a[][]= {{1,2,3},{4,5,6},{7,8,9}};    
		System.out.println("Original Matrix: \n");  
		//loop for rows  
		for(int i=0;i<3;i++)  
		{  
		//loop for columns  
		for(int j=0;j<3;j++)  
		{  
		//prints the elements of the original matrix  
		System.out.print(" "+a[i][j]+"\t");  
		}  
		System.out.println("\n");  
		}  
		System.out.println("Rotate Matrix by 90 Degrees Clockwise: \n");  
		for(int i=0;i<3;i++)  
		{  
		for(int j=2;j>=0;j--)  
		{  
		//prints the elements of the rotated matrix  
		System.out.print(""+a[j][i]+"\t");  
		}  
		System.out.println("\n");  
		}  
	}

}

//Create a student class with the following data members:- rollNo, Name,
//Course, Mark, grade, result. Develop function members to
//a. assign values for rollNo, name, course and mark.
//b. Find out the grade for the student(if mark &gt;90, then grade is A, if
//mark is between 80 and 90, then grade is B, if mark is between 70
//and 80, then grade is C, if mark is between 60 and 70, then grade
//is D, otherwise, grade is F.
//c. Find the result of the student. If mark&gt;60, then the result is Pass,
//otherwise Fail
//d. Print out the details of the student

package assignment2;

public class Question8 {
	
		private int rollNo;
		private String name,course,result;
		private double marks;
		private char grade;
		
		public void acceptDetails(int rollNo,String name,String course,double marks)
		{
			this.rollNo=rollNo;
			this.name=name;
			this.course=course;
			this.marks=marks;	
		}
		
		public char calGrade(double marks)
		{
			if(marks>90)
			{
				return grade='A';
			}
			else if(marks>=80 && marks<=90)
			{
				return grade='B';
			}
			else if(marks>=70 && marks<=80)
			{
				return grade='C';
			}
			else if(marks>=60 && marks<=70)
			{
				return grade='D';
			}
			else
			{
				return grade='F';
			}
			
		}
		public String calResult(double marks)
		{
			if(marks>=60)
			{
				return result="Pass";
			}
			else {
				return result="Fail";
			}
		}
		
		public void display()
		{
			System.out.println("---------------Student Details------------------");
			
			System.out.println("Roll Number : "+rollNo);
			System.out.println("Name        : "+name);
			System.out.println("Course      : "+course);
			System.out.println("Marks       : "+marks);
			calGrade( marks);
			calResult(marks);
			System.out.println("Result      : "+result);
			System.out.println("Grade       : "+grade);
			
		}	
		
		public static void main(String[] args)
		{
			Question8 student=new Question8();
			int rollNo;
			String name,course,result;
			double marks;
			char grade;
			student.acceptDetails(2, "Pallavi", "DAC", 86.26);
//			student.calGrade(86.34);
//			student.calResult(86.34);
			student.display();
		}
	}
package practicemodule;
public class Account {
	protected String AccountNum;
	protected double balance;
	public Account() {
		// TODO Auto-generated constructor stub
	}
	public Account(String accountNum) {
		super();
		AccountNum = accountNum;
		balance = 0;
	}

	public void deposit(double amt) {
		balance=balance+amt;
	}
	public void withdraw(double amt) {
		if(balance>amt)
		balance=balance-amt;
		else
			System.out.println("balance is less");
	}
	void details()
	{
		System.out.println("Account number:"+AccountNum);
		System.out.println("Balance is:"+balance);
		
	}
	

}

 package practicemodule;
public class SavingAccount extends Account {
	double intRate;
	public SavingAccount() {
		// TODO Auto-generated constructor stub
	}
	public SavingAccount(String accountNum,double intRate) {
		super(accountNum);
		this.intRate = intRate;
	}
	public double addInterest()
	{
		double interest=balance*intRate;
		balance=balance+interest;
		return interest;
	}
	

}
 class LoanAccount extends Account{
	double LoanAmount;

	public LoanAccount(String accountNum, double loanAmount) {
		super(accountNum);
		LoanAmount = loanAmount;
		}
	
	public void  payEmi(double emi)
	{
		
		LoanAmount=LoanAmount-emi;
		System.out.println("successful");
	}
	
	}
 
 class HousingLoan extends LoanAccount{
	 int tenure;

	public HousingLoan(String accountNum, double loanAmount, int tenure) {
		super(accountNum, loanAmount);
		this.tenure = tenure;
	}

	public void extendTenure(int yr)
	{
	tenure=tenure+yr;
	System.out.println("Tenure extended by"+yr+"years");
		
	}
	 
 }
 
package practicemodule;
public class MainAccount {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		SavingAccount sa=new SavingAccount("SBI2001", 0.05);
//		sa.details();
		sa.deposit(5000);
		sa.details();
		System.out.println("--------------------------------");
//		sa.addInterest();
//		sa.details();
		HousingLoan ha=new HousingLoan("HL2027", 60000, 10);
		ha.deposit(15000);
		ha.payEmi(5000);
		ha.details();
		


	}

}
