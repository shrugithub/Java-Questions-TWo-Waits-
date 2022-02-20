# Java-Questions-TWo-Waits-

**Write a Java program to perform basic Calculator operations.

import java.util.Scanner;
public class Calculator {
   public static void main(String[] args) {
      double num1;
      double num2;
      double ans;
      char op;
      Scanner reader = new Scanner(System.in);
      System.out.print("Enter two numbers: ");
      num1 = reader.nextDouble();
      num2 = reader.nextDouble();
      System.out.print("\nEnter an operator (+, -, *, /): ");
      op = reader.next().charAt(0);
      switch(op) {
         case '+': ans = num1 + num2;
            break;
         case '-': ans = num1 - num2;
            break;
         case '*': ans = num1 * num2;
            break;
         case '/': ans = num1 / num2;
            break;
      default: System.out.printf("Error! Enter correct operator");
         return;
      }
      
  output:    Enter two numbers: 10.0 7.0
Enter an operator (+, -, *, /): -
The result is given as follows:
10.0 - 7.0 = 3.0


**Write a Java program to calculate Fibonacci Series up to n numbers.**
class Main {
  public static void main(String[] args) {

    int n = 10, firstTerm = 0, secondTerm = 1;
    System.out.println("Fibonacci Series till " + n + " terms:");

    for (int i = 1; i <= n; ++i) {
      System.out.print(firstTerm + ", ");

      // compute the next term
      int nextTerm = firstTerm + secondTerm;
      firstTerm = secondTerm;
      secondTerm = nextTerm;
    }
  }
  
  
  output:   Fibonacci Series till 10 terms:
0, 1, 1, 2, 3, 5, 8, 13, 21, 34



**Write a Java program to calculate a Factorial of a number.
  
  public class Factorial {

    public static void main(String[] args) {

        int num = 10;
        long factorial = 1;
        for(int i = 1; i <= num; ++i)
        {
            // factorial = factorial * i;
            factorial *= i;
        }
        System.out.printf("Factorial of %d = %d", num, factorial);
    }
}



output: 
Factorial of 10 = 3628800

**Write a Java program to find out whether the given String is Palindrome or not.
**
class Main {
  public static void main(String[] args) {

    String str = "Radar", reverseStr = "";
    
    int strLength = str.length();

    for (int i = (strLength - 1); i >=0; --i) {
      reverseStr = reverseStr + str.charAt(i);
    }

    if (str.toLowerCase().equals(reverseStr.toLowerCase())) {
      System.out.println(str + " is a Palindrome String.");
    }
    else {
      System.out.println(str + " is not a Palindrome String.");
    }
  }
}

output:   Radar is a Palindrome String.

**Write a Java program to calculate Permutation and Combination of 2 numbers.**


public class Example {
   static int factorial(int n) {
      int fact = 1;
      int i = 1;
      while(i <= n) {
         fact *= i;
         i++;
      }
      return fact;
   }
   public static void main(String args[]) {
      int n = 7, r = 3, comb, per;
      per = factorial(n) / factorial(n-r);
      System.out.println("Permutation: " + per);
      comb = factorial(n) / (factorial(r) * factorial(n-r));
      System.out.println("Combination: " + comb);
   }
}

output:
Permutation: 210
Combination: 35


**Write a program in Java to print Diamond Pattern.
**


import java.util.Scanner;
public class Exercise21 {

  public static void main(String[] args)
	  
	  
{
   int i,j,r;
   System.out.print("Input number of rows (half of the diamond) : ");
   Scanner in = new Scanner(System.in);
		    r = in.nextInt();
   for(i=0;i<=r;i++)
   {
     for(j=1;j<=r-i;j++)
     System.out.print(" ");
     for(j=1;j<=2*i-1;j++)
       System.out.print("*");
     System.out.print("\n");
   }
 
   for(i=r-1;i>=1;i--)
   {
     for(j=1;j<=r-i;j++)
     System.out.print(" ");
     for(j=1;j<=2*i-1;j++)
       System.out.print("*");
     System.out.print("\n");
   }
 
}
}

output:

Input number of rows (half of the diamond) : 7                                                                                                       
      *                                                                                                       
     ***                                                                                                      
    *****                                                                                                     
   *******                                                                                                    
  *********                                                                                                   
 ***********                                                                                                  
*************                                                                                                 
 ***********                                                                                                  
  *********                                                                                                   
   *******                                                                                                    
    *****                                                                                                     
     ***                                                                                                      
      *
      
      
    **  Write a Java Program to reverse the letters present in the given String.
**
import java.io.*;
import java.util.Scanner;
 
class GFG {
    public static void main (String[] args) {
       
        String str= "Geeks", nstr="";
        char ch;
       
      System.out.print("Original word: ");
      System.out.println("Geeks"); //Example word
       
      for (int i=0; i<str.length(); i++)
      {
        ch= str.charAt(i); //extracts each character
        nstr= ch+nstr; //adds each character in front of the existing string
      }
      System.out.println("Reversed word: "+ nstr);
    }
}


**Write a Java Program to check whether the given array is Mirror Inverse or not
**

public class mirror {
 
    // Function that returns true if
    // the array is mirror-inverse
    static boolean isMirrorInverse(int arr[])
    {
        for (int i = 0; i < arr.length; i++) {
 
            // If condition fails for any element
            if (arr[arr[i]] != i)
                return false;
        }
 
        // Given array is mirror-inverse
        return true;
    }
 
    // Driver code
    public static void main(String[] args)
    {
        int arr[] = { 1, 2, 3, 0 };
        if (isMirrorInverse(arr))
            System.out.println("Yes");
        else
            System.out.println("No");
    }
    
    output: NO 
      
      
     ** Write a Java program to remove elements from an ArrayList
     
     
import java.util.ArrayList;
import java.util.List;
 
// Main class
public class rEmove {
    // Main driver method
    public static void main(String[] args)
    {
        // Creating an object of List interface with
        // reference to ArrayList class
        List<Integer> al = new ArrayList<>();
 
        // Adding elements to our ArrayList
        // using add() method
        al.add(10);
        al.add(20);
        al.add(30);
        al.add(1);
        al.add(2);
 
        // Printing the current ArrayList
        System.out.println(al);
 
        // This makes a call to remove(int) and
        // removes element 20
        al.remove(1);
 
        // Now element 30 is moved one position back
        // So element 30 is removed this time
        al.remove(1);
 
        // Printing the updated ArrayList
        System.out.println(al);
    }
}
  
  output:   
  [10, 20, 30, 1, 2]
[10, 1, 2]

  
 ** Write a Java Program to find the Transpose of a given Matrix.**

public class MatrixTransposeExample{  
public static void main(String args[]){  
//creating a matrix  
int original[][]={{1,3,4},{2,4,3},{3,4,5}};    
    
//creating another matrix to store transpose of a matrix  
int transpose[][]=new int[3][3];  //3 rows and 3 columns  
    
//Code to transpose a matrix  
for(int i=0;i<3;i++){    
for(int j=0;j<3;j++){    
transpose[i][j]=original[j][i];  
}    
}    
  
System.out.println("Printing Matrix without transpose:");  
for(int i=0;i<3;i++){    
for(int j=0;j<3;j++){    
System.out.print(original[i][j]+" ");    
}    
System.out.println();//new line    
}    
System.out.println("Printing Matrix After Transpose:");  
for(int i=0;i<3;i++){    
for(int j=0;j<3;j++){    
System.out.print(transpose[i][j]+" ");    
}    
System.out.println();//new line    
}    
}}  
  
  
  output: 
  
  Printing Matrix without transpose:
1 3 4 
2 4 3 
3 4 5 
Printing Matrix After Transpose:
1 2 3 
3 4 4 
4 3 5


























