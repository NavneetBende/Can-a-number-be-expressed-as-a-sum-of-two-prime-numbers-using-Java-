# Can-a-number-be-expressed-as-a-sum-of-two-prime-numbers-using-Java-

Can a number be expressed as a sum of two prime numbers using java
Here, we will discuss program to check whether a number be expressed as a sum of two prime numbers using java.  we will ask the user to enter a positive integer and check whether that number can be expressed as the sum of two prime numbers. If that number can be expressed as sum of two prime numbers then print the numbers in the output and else print the statement that the number cannot be expressed as a sum of two prime numbers.

Number be expressed as a sum of two prime numbers using java
Theory
There are many theories which express numbers as a sum of two primes like Goldbach’s Conjecture which states that any even number greater than 2 can be expressed as a sum of two primes.

Prime number is a number which only have two divisors i.e. a number which can not be divided by any other number other than 1 or itself is a prime number.

Here we will check for all the numbers if they can be expressed as sum of two primes or not.

Algorithm
Take number as input in n
Initialize a variable flag as 0
Iterate using for loop from value of i between (2, n/2)
 For each iteration Call a function sum_of_two_primes for value of i is it returns 1
Call same function for value n-i and if it is also 1 then print i and n-i as answer increment the flag to 1
If flag is 0 print not possible
Create function sum_of_two_prime where check if passed number is prime return true else false

Java code
Run
//Java program to check whether a number can be expressed as a sum of two prime numbers
import java.util.Scanner;
public class Main
{
	public static void main(String[] args)
	{
		//scanner class declaration
		Scanner sc = new Scanner(System.in);
		//input from user
		System.out.print("Enter a number : ");				
		int number = sc.nextInt();
		int x = 0;
		for(int i = 2 ; i <= number/2 ; i++)
		{
			if(prime_or_not(i) == 1)
			{
				if(prime_or_not(number-i) == 1)
				{
					System.out.println(number+ " = "+i+" + "+(number-i));
					x = 1;
				}
			}
		}
		if(x == 0)
			System.out.println(+number+" cannot be expressed as a sum of two prime numbers");
	}
        //function for checking number is prime or not
	public static int prime_or_not(int n)
	{
		int c = 1;
		for(int i = 2 ; i < n ; i++)
		{
			if(n % i == 0)
			{
				c = 0;
				break;
			}
		}
		return c;
	}
}
Output
Enter a number : 14
14 = 3 + 11
14 = 7 + 7
