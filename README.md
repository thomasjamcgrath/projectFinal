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
        cout << "The sum is " << percent << ".\n";r
    }

}
