# Codesofttask
[23/08, 10:38 pm] Prathmesh Patil Kodoli: # include <iostream>
using namespace std;

int main() {

  char op;
  float num1, num2;

  cout << "Enter operator: +, -, *, /: ";
  cin >> op;

  cout << "Enter two operands: ";
  cin >> num1 >> num2;

  switch(op) {

    case '+':
      cout << num1 << " + " << num2 << " = " << num1 + num2;
      break;

    case '-':
      cout << num1 << " - " << num2 << " = " << num1 - num2;
      break;

    case '*':
      cout << num1 << " * " << num2 << " = " << num1 * num2;
      break;

    case '/':
      cout << num1 << " / " << num2 << " = " << num1 / num2;
      break;

    default:
      // If the operator is other than +, -, * or /, error message is shown
      cout << "Error! operator is not correct";
      break;
  }

  return 0;
}
[23/08, 10:38 pm] Prathmesh Patil Kodoli: #include<iostream>
using namespace std;
int main()
{
    int i;
    float mark, sum=0, avg;
    cout<<"Enter Marks obtained in 5 Subjects: ";
    for(i=0; i<5; i++)
    {
        cin>>mark;
        sum = sum+mark;
    }
    avg = sum/5;
    cout<<"\nGrade = ";
    if(avg>=91 && avg<=100)
        cout<<"A1";
    else if(avg>=81 && avg<91)
        cout<<"A2";
    else if(avg>=71 && avg<81)
        cout<<"B1";
    else if(avg>=61 && avg<71)
        cout<<"B2";
    else if(avg>=51 && avg<61)
        cout<<"C1";
    else if(avg>=41 && avg<51)
        cout<<"C2";
    else if(avg>=33 && avg<41)
        cout<<"D";
    else if(avg>=21 && avg<33)
        cout<<"E1";
    else if(avg>=0 && avg<21)
        cout<<"E2";
    else
        cout<<"Invalid!";
    cout<<endl;
    return 0;
}
[23/08, 10:38 pm] Prathmesh Patil Kodoli: #include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main()
{
	int num, guess, tries = 0;
	srand(time(0)); //seed random number generator
	num = rand() % 100 + 1; // random number between 1 and 100
	cout << "Guess My Number Game\n\n";

	do
	{
		cout << "Enter a guess between 1 and 100 : ";
		cin >> guess;
		tries++;

		if (guess > num)
			cout << "Too high!\n\n";
		else if (guess < num)
			cout << "Too low!\n\n";
		else
			cout << "\nCorrect! You got it in " << tries << " guesses!\n";
	} while (guess != num);

	return 0;
}
[23/08, 10:38 pm] Prathmesh Patil Kodoli: #include <iostream>
#include <fstream>
using namespace std;
int main()
{
 ifstream fin("fname.txt"); //opening text file
 int word=1; //will not count first word so initial value is 1
 char ch;
 fin.seekg(0,ios::beg); //bring position of file pointer to begining of file
 
 while(fin)
 {
  fin.get(ch);
  if(ch==' '||ch=='\n')
   word++;
 } 
 
 cout<<"\nWords="<<word<<"\n";
 fin.close(); //closing file
 
 return 0;
}
