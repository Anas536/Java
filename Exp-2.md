## Aim:
Create two methods:

Get the input for radius from the user.

double getArea(double r) → calculate the area and return the area(Don't print anything in this method).

void printArea(double area) → pass the calculated area to this method and print the area of a circle.

## Program:

```
import java.util.Scanner;

class prog {

    static double getArea(double r) {
        return 3.14 * r * r;
    }

    static void printArea(double area) {
        System.out.printf("%.2f",area);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double radius = sc.nextDouble();
        double area = getArea(radius);
        printArea(area);

        sc.close();
    }
}

```
