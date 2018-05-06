#include <iostream>
#include <string>
#include <sstream>
#include <stdlib.h>
#include <stdio.h>

/// functions being declared
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

struct tax_T {     ///sales tax structure and pointer
  string product;
  int salesTax;
  int amount;
  double tranAmn = 0;
  double finalTax= 0;
};

int main()
{
  cout << welcome ();
  initials();
  _sleep(1000);
  secMenu(mainMenu());
  _sleep(5000);
  goodBye;
 }
 
 


