## Aim:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## Program:

```
import java.util.Scanner;

public class Main{
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        
        String a = null;
        
        try {
            a = input.next();
            if(a.equalsIgnoreCase("null")){
                throw new NullPointerException();
            }
            System.out.println(a.toUpperCase());
        } catch(NullPointerException e){
            System.out.println("Null element");
        }
    }
}
```
