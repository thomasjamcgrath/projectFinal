#include <iostream>
#include <string>
#include <sstream>
#include <stdlib.h>
#include <stdio.h>

using namespace std;

///functions being declared

string welcome(string hello = "Hello User!\n");

int main();

void percentMenu(); ///functions for the percent calculation
int percentFind();
int percentFirstAmn();
void percentCalc(double& percentage, double& percentAmn);


void initials();
void goodBye();

void clearScreen();


int mainMenu();
void secMenu(int selection);
void calcMenu();


void add();
void sub();
void div();
void mult();

void mean();        

void salesTax();   


struct tax_T {     
    string product;
    int salesTax;
    int amount;
    double tranAmn = 0;
    double finalTax = 0;
};

int main()
{
    cout << welcome();
    initials();
    _sleep(1000);
    secMenu(mainMenu());
    _sleep(5000);
    goodBye();

}

enter string here cosmo

int mainMenu()
{

    int selection = 0;
                                            
    cout << "Press 1 for:\t Calculator\n";
    cout << "Press 2 for\t Percent Calculation\n";
    cout << "Press 3 for:\t Sales Tax\n";
    cout << "Press 4 for:\t Average\n";

    cin >> selection;
    cin.ignore();

    return selection;

}

enter secmenu here cosmo

void calcMenu()
{

    int ans = 0;
    int userInput = 0;
    int debug = 4;

    cout << "Welcome to the Calculator.\n";
    cout << "Press 1:\t Continue.\n";
    cout << "Press 2:\t Back to selections.\n";
    cin >> ans;

if (ans == 1)
{
        do
        {
            cout << "Press 1:\t Addition\n";
            cout << "Press 2:\t Subtraction\n";
            cout << "Press 3:\t Multiplication\n";
            cout << "Press 4:\t Division\n";
            cout << "Press 5:\t To Quit\n";
            cin >> userInput;

            switch (userInput)
            {
                case 1:
                    add();
                    break;
                case 2:
                    sub();
                    break;
                case 3:
                    mult();
                    break;
                case 4:
                    div();
                    break;
            }

            userInput = 5;


        } while (userInput!= 5);

        ans = 2;

}else

    {

        main();

    }

}

void add()
{
    clearScreen();

    int terms = 0;
    double sum = 0;
    int x = 1;


    cout << "Welcome to Addition.\n";
    cout << "Enter the amount of values.\n";
    cin >> terms;
    cout << "Enter the values.\n";

    const int NUM_VALUES = terms;///values used in the array and adding the values inside the array
    int add[NUM_VALUES];

    for (int i = 0; i < terms; i++)
        {

            add[i] = 0;

        }


    for (int i = 0; i < terms; i++)
    {

        cin >> add[i];

    }

    for (int i = 0; i < terms; i++)
        {

            sum = sum + add[i];

        }

        cout <<  "The sum is " << sum << "\n";

}

void sub()
{
    clearScreen();

    int terms = 0;
    double sum = 0;
    int subNum = 0;


    cout << "Welcome to Subtract.\n";
    cout << "Enter what you are subtracting from.\n";
    cin >> subNum;
    cout << "Enter the amount of values you are subtracting.\n";
    cin >> terms;
    cout << "Enter the values.\n";

    const int NUM_VALUES = terms;
    int sub[NUM_VALUES];

    for (int i = 0; i < terms; i++)
        {


            sub[i] = 0;

        }


for (int i = 0; i < terms; i++)
    {

        cin >> sub[i];

    }

    for (int i = 0; i < terms; i++)
        {

            sum = sum - sub[i];

        }

            cout << "The sum is " << sum << "\n";

}

void mult()
{
    clearScreen();

    int terms = 0;
    double sum = 1;
    int x = 1;

    cout << "Welcome to Multiplication.\n";
    cout << "Enter the amount of values.\n";
    cin >> terms;///value for array input
    cout << "Enter the values.\n";

    const int NUM_VALUES = terms;
    int mult[NUM_VALUES];

    for (int i = 0; i < terms; i++)
        {

            mult[i] = 0;

        }


for (int i = 0; i < terms; i++)
    {

        cin >> mult[i];

    }

    for (int i = 0; i < terms; i++)
        {

            sum = sum * mult[i];

        }

            cout << "The sum is " << sum << "\n" ;
}

void div()
{
    clearScreen();

    int terms = 0;
    double sum = 0;
    double divNum;


    cout << "Welcome to Division.\n";
    cout << "Enter what you are dividing from.\n";
    cin >> divNum;///must have number to divide by
    cout << "Enter the amount of values.\n";
    cin >> terms;
    cout << "Enter the values.\n";

    const int NUM_VALUES = terms;
    int div[NUM_VALUES];

    for (int i = 0; i < terms; i++)
        {

            div[i] = 0;

        }


for (int i = 0; i < terms; i++)
    {

        cin >> div[i];

    }

    for (int i = 0; i < terms; i++)
        {

            sum = divNum / div[i];

        }


            cout << "The sum is " << sum << "\n";

}

void mean()
{
    clearScreen;///clear screen
    
    int terms = 0;
    int sum = 0;
    int x = 1;
    
    cout << "Welcome to Finding the Mean. \n";
    cout << "Enter the amount of Values. \n";
    cin >> terms; ///number of terms to find mean
    cout << "Enter the values. \n";
    
    const int NUM_VALUES = terms; ///used for array
    int add[NUM_VALUES];
    
    for (int i = 0; i < terms, i++)
        {
            add[i] = 0;
            
        }
        
        for (int i = 0; i < terms; i++) /// in array before addition can take place.
          {   
        
            cin >> add[i];
         }
        
        for (int i = 0; i < terms; i++)///finds the sum of the array
        
        {
            
            sum = sum + add [i];
            
        }
        
            cout << "The mean is " << sum / terms;/// divides array by amount of terms.
 }
        

void salesTax()
{
    clearScreen();

    string tax;

    tax_T aTax;
    tax_T * pTax;
    pTax = &aTax;
    double tranAmn = 0;
    double finalTax = 0;
    double finalSum = 0;
    double sum = 0;
    double startTax = 0;

    cout << "Enter the name of your transaction.\n";
    getline (cin, pTax->product);

    cout << "Enter the number of items." << endl;
    getline (cin, tax);

    cout << "Enter the amount of the transaction\n";
    cin >> tranAmn;

    cout << "Enter the sales tax\n";
    cin >> startTax;

    (stringstream) tax >> pTax->amount;

    cout << endl << "You have entered:\t";
    cout << pTax-> product;
    cout << " (" << pTax->amount << ")\n";

    finalTax = startTax / 100;

    sum = tranAmn * finalTax;
    finalSum = tranAmn + sum;

    cout << "The final sum is: "<< finalSum;


}

void initials()
{
    _sleep(1000);
    clearScreen();
    
    char firstIn;
    char secondIn;
    
    bool x;
    
    int ans = 0;
    
    cout << "Enter the first intial. \n";///asks user for first initial
    cin >> secondIn;
    
    cout << "Press 1:\t If you are ready to continue. \n";
    cin >> ans;
    
    if (ans == 1) /// bool used to decided if initials are correct
    {
        bool x = true;
    }

clearScreen();

    if ( x == true)
    {
        cout << "Hello " << firstIn << secondIn << ".\n";
    }
}

/**
clearScreen
    function clears screen by inputing \n one hundred times
        no parameters
            no return
*/

void clearScreen()
{
    system("cls");
}

/**
goodBye
    outputs GOODBYE to user
        no parameters
            no return
*/
void goodBye()
{
    clearScreen();
    cout << "Created by Thomas McGrath\n";
    cout << "And Connor Cosmo\n";
    cout << "GOODBYE USER\n";
}

void percentMenu()
{
    clearScreen();

    double percentage = 0;

    cout << "Welcome to percent calculation.\n";
    cout << "Enter the percent:\t\n";
    cin >> percentage;

    double percentAmn = 0;

    cout << "Enter the number that you want to add or subtract the percentage too:\n";
    cin >> percentAmn;


    percentCalc(percentage, percentAmn);
}

void percentCalc(double& percentage, double& percentAmn)
{
    double percent = 0;
    double percentHolder;
    int ans = 0;

    cout << "Enter 1: To add the percentage.\n";
    cout << "Enter 2: to subtract the percentage.\n";
    cin >> ans;

    if (ans == 1)
    {
        percentHolder = percentAmn * percentage / 100;
        percent = percentAmn + percentHolder;
        cout << "The sum is " << percent << ".\n";
    }
    else if (ans == 2)
    {
        percentHolder = percentAmn * percentage / 100;
        percent = percentAmn - percentHolder;
        cout << "The sum is " << percent << ".\n";
    }

}
