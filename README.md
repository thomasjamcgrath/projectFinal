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
