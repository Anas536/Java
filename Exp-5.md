## Aim:
You are writing a Java program where you read a string input. If the input is "init", you create an object and call its method. If it's "null", no object is created.
Your program crashes with a NullPointerException when "null" is entered.
What caused the crash and how can you handle it to prevent the error?

## Program:

```
import java.util.Scanner;

class MyClass{
    void show(){
        System.out.println("Object exists");
    }
}

public class Main{
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        
        String a = null;
        
        try{
            a = input.nextLine();
            if(a.equalsIgnoreCase("null")){
                throw new NullPointerException();
            }
            MyClass obj = new MyClass();
            obj.show();
        }catch (NullPointerException e){
            System.out.println("Object is null");
        }
    }
}
```
