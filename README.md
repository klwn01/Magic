
// Write a program to check if a number is a magic or not.
// A magic number is an integer in which permutations of the digits are successive multiples
// of the number (number of digits and order does not change, but can start from different position)
// inp. e.g. 142857


import java.util.Scanner;
import java.util.Arrays;

public class Main {


    public static void main(String[] args) {


        Scanner input = new Scanner(System.in);
        System.out.print("Input a number: ");
        int num = input.nextInt();

        int i, mult, x, z, y, k = 0;
        String temp;
        char b[];

        // Converting integer to string (for sort purpose)
        String str = Integer.toString(num);

        // Add string to array and sort
        char a[] = str.toCharArray();
        Arrays.sort(a);


        for (i=2; i<=a.length; i++ ) {

            mult = num * i;

         // Converting integer to string (for sort purpose)
            temp = Integer.toString(mult);
            b = temp.toCharArray();
            Arrays.sort(b);

          // Converting string back to integer (for comparision)
            x = Integer.parseInt(new String(a));
            z = Integer.parseInt(new String(b));

         // Compare values
            if (x!=z){
                System.out.println("It is NOT!");
                break;
            }
            k =+i;

        }
         //
        if (k>2) {
            System.out.println("It's magic!");
        }
    }
}
