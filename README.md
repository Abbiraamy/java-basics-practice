import java.util.Scanner;

public class PrimitiveAndInputDemo {

    // Static variable (class-level)
    static int staticCount = 10; 
    // static used because it is shared across all objects

    // Instance variable (object-level)
    double instanceSalary = 25000.50;
    // double used for salary to store decimal values accurately

    public static void main(String[] args) {

        // Local variables (method-level)
        int localAge = 22;
        // int is sufficient for age, memory efficient (4 bytes)

        /* 1. Primitive Data Types & Memory Usage */
        byte b = 10;        // 1 byte
        short s = 200;      // 2 bytes
        int i = 1000;       // 4 bytes
        long l = 100000L;   // 8 bytes
        float f = 10.5f;    // 4 bytes
        double d = 99.99;   // 8 bytes
        char c = 'A';       // 2 bytes
        boolean flag = true; // JVM dependent (usually 1 byte)

        // 2. Scanner class for multiple inputs
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.print("Enter two numbers: ");
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        // 5. Handling invalid input using condition
        if (num2 == 0) {
            System.out.println("Division by zero is not allowed!");
        } else {

            // 3. Arithmetic operations
            int sum = num1 + num2;
            int diff = num1 - num2;
            int prod = num1 * num2;
            int div = num1 / num2;

            // 6. Formatted output
            System.out.printf("Sum = %d, Difference = %d, Product = %d, Division = %d%n",
                    sum, diff, prod, div);
        }

        // 4. Type casting
        double castDouble = i;        // implicit casting (int → double)
        int castInt = (int) d;        // explicit casting (double → int)

        System.out.println("Implicit Cast (int to double): " + castDouble);
        System.out.println("Explicit Cast (double to int): " + castInt);

        // 7. Local, instance, static variable demonstration
        PrimitiveAndInputDemo obj = new PrimitiveAndInputDemo();

        System.out.println("Local variable (age): " + localAge);
        System.out.println("Instance variable (salary): " + obj.instanceSalary);
        System.out.println("Static variable (count): " + staticCount);

        sc.close();
    }
}
