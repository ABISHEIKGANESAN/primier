# primier

Python program to print all Prime numbers in an Interval :

Given two positive integers start and end. 
The task is to write a Python program to print all Prime numbers in an Interval.

Definition: 
A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself. The first few prime numbers are {2, 3, 5, 7, 11, ….}.
The idea to solve this problem is to iterate the val from start to end using a for loop and for every number, if it is greater than 1, check if it divides n. If we find any other number which divides, print that value.
Below is the Python implementation:

Code :
public class Prime {

    public static void main(String[] args) {  //prime number which has no positive divisors other than 1

        int low = 20, high = 50;              

        while (low < high) {
            boolean flag = false;

            for(int i = 2; i <= low/2; ++i) {
                // condition for nonprime number
                if(low % i == 0) {
                    flag = true;
                    break;
                }
            }

            if (!flag && low != 0 && low != 1)
                System.out.print(low + " ");

            ++low;
        }
    }
}
