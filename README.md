DATA TYPES

using System;

class Program 
{ 
    static void Main() 
    { 
        Console.Write("Enter your name: "); 
        string name = Console.ReadLine(); 

        Console.Write("Enter your age: "); 
        int age = int.Parse(Console.ReadLine()); 

        Console.Write("Enter your address: "); 
        string address = Console.ReadLine(); 

        Console.Write("Enter your weight (in lbs): "); 
        float weight = float.Parse(Console.ReadLine()); 

        Console.Write("Enter your height (in meters): "); 
        float height = float.Parse(Console.ReadLine()); 

        Console.WriteLine($"\nHello, my name is {name}. I am {age} years old, I live at {address}, I am {height} meters tall, and I weigh {weight}lbs."); 
    } 
}

==========================================================
SWITCH CASE AND LOOPS (CALCULATOR)

using System;

class Program
{
    static void Main(string[] args)
    {
        while (true)
        {
            float result = 0;
            
            Console.WriteLine("Enter first number: ");
            float num1 = float.Parse(Console.ReadLine());

            Console.WriteLine("Enter second number: ");
            float num2 = float.Parse(Console.ReadLine());

            Console.WriteLine("Enter operator (+, -, *, /): ");
            string op = Console.ReadLine();

            switch (op) 
            {
                case "+": 
                    result = num1 + num2;
                    break;
                case "-":
                    result = num1 - num2;
                    break;
                case "*":
                    result = num1 * num2;
                    break;
                case "/":
                    result = num1 / num2;
                    break;
		default:
                    Console.WriteLine("Invalid operator. Try again.");
        	    continue;
		    
		
            }
            Console.WriteLine("Result = " + result);

            Console.Write("Do you want to calculate again? (y/n): ");
            string choice = Console.ReadLine().ToLower();


            if (choice != "y" && choice != "yes")
            {
                Console.WriteLine("Goodbye!");
                break; 
            }
        }
    }
}
