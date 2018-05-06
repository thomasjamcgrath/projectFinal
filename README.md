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

    const int NUM_VALUES = terms;
    int add[NUM_VALUES];

    for (int i = 0; i < terms; i++)/
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
