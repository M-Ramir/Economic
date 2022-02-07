# Economic
////////////////////////////////////////////////////////////////////
// Maria Ramirez
// TINFO-200C
// L2vs
////////////////////////////////////////////////////////////////////
// Change History
// Date              Developer         Description           
// 2022-01-15        Maria Ramirez     File and class creation and initial testing for submission
//
//////////////////////////////////////////////////////////////////////
/// This program asks users a series of questions such as name, their trip destination,
/// amount of miles driven, and amount of fuel used. With this information the program
/// calculates their miles per gallon and lets the user know if their trip was 
/// economical and if their miles per gallon was very good/good/poor.



using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;


namespace Economic
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Line produces an output for user.
            // Describes the program and information needed from user.
            Console.WriteLine(@"
            ** WELCOME TO THE ECONOMIC TRIP CALCULATOR **
            ** This program will help you determine how **
            ** efficient and economical your trips are!***
            ********** LETS GET STARTED! ***************");

            // Get's the users name first
            // uses string to store name for later use
            Console.Write("Enter your name (ex. Bob): ");
            string nameOfuser = Console.ReadLine();

            // next prompt will ask user for destination
            // uses string to store destination for later use
            Console.Write("Enter your destination (ex. Florida): ");
            string nameOfdestination = Console.ReadLine();

            // Prompts user to enter amount of miles to get to their destination
            // Saves their imput as an int for later use when finding the mpgs
            Console.Write("How many miles did it take to get to your destination? (ex. 900, 200): ");
            int milesDriven = int.Parse(Console.ReadLine());

            // Asks user for amount of fuel used
            // Saves their imput as a double for later use so mpgs can be more accurate
            Console.Write("Enter amount of fuel used (ex.9.9, 3.2): ");
            double gallonsUsed = double.Parse(Console.ReadLine());


            // processing - do the calculations (mixed mode)
            double mpg = milesDriven / gallonsUsed;

            // if the calculations above say the mpg is over or equal to 30.0 the prompt below prints out
            if (mpg >= 30)

            {   // prints out imput user has given, name and place of destination
                Console.WriteLine($"{nameOfuser},your trip to {nameOfdestination} was very economical. \n");
                // prints out users miles driven and gallons used ( user gave us this information)
                Console.WriteLine($"You traveled {milesDriven} miles to reach your destination using only {gallonsUsed} gallons of fuel! \n");
                // uses math on line 60 and outprints it here as well as a statment regarding thier mpgs
                Console.WriteLine($"Your fuel efficiency rating on this trip was {mpg} miles per gallon!");
                // prints mpg and tells user their fuel efficiency being over 30 is very good!
                Console.WriteLine($"With an MPG rating of over 30.0, this is considered very good.");
            }
            // if the calculations above say the mpg is above 20 mpgs and below 30 mpgs then the prompt below prints out
            else if (mpg > 20 && mpg > 30)

            {   // prints out imput user has given, name and place of destination
                Console.WriteLine($"{nameOfuser},your trip to {nameOfdestination} was economical.");
                // prints out users miles driven and gallons used ( user gave us this information)
                Console.WriteLine($"You traveled {milesDriven} miles to reach your destination using {gallonsUsed} gallons of fuel.");
                // uses math on line 60 and outprints it here as well as a statment regarding thier mpgs
                Console.WriteLine($"Your fuel efficiency rating on this trip was {mpg} mpg!");
                // prints mpgs and tells user their fuel efficiency is good
                Console.WriteLine($"With an MPG rating of approaching 30.0, this is considered good.");

            }
            // if the calculations above say the mpg is below 20 mpgs then the prompt below prints out.
            else if (mpg < 20)
            {   // prints out imput user has given, name and place of destination
                Console.WriteLine($"{nameOfuser},your trip to {nameOfdestination} was NOT very economical.");
                // prints out users miles driven and gallons used ( user gave us this information)
                Console.WriteLine($"You traveled {milesDriven} to reach your destination, but your vehicle used {gallonsUsed}");
                // uses math on line 60 and outprints it here as well as a statment regarding thier mpgs
                Console.WriteLine($"gallons of fuel." + $"This is only {mpg} mpg!");
                // prints mpgs and tells user their fuel efficiency is concerning!
                Console.WriteLine($"With an MPG rating was under 20.0, this is cause for concern.");

            }
            // Sign off for user and ends program
            Console.WriteLine("Thank you for using the Mileage Trip Calculator!");




        }

    }
}
