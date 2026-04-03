## Aim:
Write a Java program to:

    Create a base class Shape with methods draw() and calculateArea().

    Create two subclasses:

        Circle: overrides draw() and calculateArea() to handle a circle.

        Cylinder: overrides draw() and overrides calculateArea() to calculate the total surface area of the cylinder 

    Take input from the user to choose between circle and cylinder, and input relevant dimensions.


## Program:
```


import java.util.Scanner;
import java.text.DecimalFormat;

class Shape{
    void draw(){
        System.out.println("Drawing a shape...");
    }
    
    double calculateArea(){
        return 0;
    }
}

class Circle extends Shape{
    
    double radius;
    
    Circle(double radius){
        this.radius = radius;
    }
    
    @Override
    void draw(){
        System.out.println("Drawing a circle...");
    }
    
    @Override
    double calculateArea(){
        
        return (Math.PI * radius * radius);
    }

}

class Cylinder extends Shape{
    double radius;
    double height;
    
    Cylinder(double radius, double height){
        this.radius = radius;
        this.height = height;
        
    }
    
    @Override
    void draw() {
        System.out.println("Drawing a cylinder...");
    }
    
    @Override
    double calculateArea(){
        return (2* Math.PI * radius * (radius + height));
    }
}

public class Main{
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        DecimalFormat df = new DecimalFormat("0.00");
        String choice = input.nextLine().trim();
        Shape s;
        if(choice.equalsIgnoreCase("circle")){
            double radius = input.nextDouble();
            s = new Circle(radius);
        } else if(choice.equalsIgnoreCase("cylinder")) {
            double radius = input.nextDouble();
            double height = input.nextDouble();
            
            s = new Cylinder(radius, height);
        } else {
            System.out.println("Invalid shape type.");
            return;
        }
        s.draw();
        System.out.println("Area: " + df.format(s.calculateArea()));
    }
}
```
