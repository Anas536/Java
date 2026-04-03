## Aim:
Lovely is learning java basics, can you teach her the different types of datatypes in java? Write a program that uses all datatypes and print them all.

Input Format:

byte - 24

short - 11000

int - 1,34,500

long - 24,23,10,34

float - 24.20

double - 1,30,000.80

boolean - true/false

char - 'u'

String -"Heyyy, Lovely, Let's learn java!"

## Program:

```

import java.util.Scanner;


public class DatatypePrinter {
    public static void main(String[] args) {
        Scanner inputScanner = new Scanner(System.in);
        byte myByte = inputScanner.nextByte();
        short myShort = inputScanner.nextShort();
        int myInt = inputScanner.nextInt();
        long myLong = inputScanner.nextLong();
        float myFloat = inputScanner.nextFloat();
        double myDouble = inputScanner.nextDouble();
        boolean myBoolean = inputScanner.nextBoolean();
        char myChar = inputScanner.next().charAt(0);
        inputScanner.nextLine();
        String myString = inputScanner.nextLine();
        System.out.println("Hey Lovely, let's print all types of data received from user using different data types");
        System.out.println("This is byte datatype " + myByte);
        System.out.println("This is short datatype " + myShort);
        System.out.println("This is int datatype " + myInt);
        System.out.println("This is long datatype " + myLong);
        System.out.println("This is float datatype " + myFloat);
        System.out.println("This is double datatype " + myDouble);
        System.out.println("This is boolean datatype " + myBoolean);
        System.out.println("This is char datatype " + myChar);
        System.out.println("This is string datatype " + myString);
    }
}
```
