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


void initials();///starting and ending functions
void goodBye();

void clearScreen();///function clears screen


int mainMenu();///menu functions
void secMenu(int selection);
void calcMenu();


void add();///calculator functions
void sub();
void div();
void mult();

void mean();        ///mean function

void salesTax();        ///sales tax function


struct tax_T {      ///sales tax structure and pointer
    string product;
    int salesTax;
    int amount;
    double tranAmn = 0;
    double finalTax = 0;
};
