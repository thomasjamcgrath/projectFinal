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
