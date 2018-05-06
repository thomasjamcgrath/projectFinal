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
