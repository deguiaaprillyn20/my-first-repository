#include <iostream>
#include <string>
#include <conio.h>

using namespace std;

int numone;
int numtwo;
int result;
char decision;
string choices;

class Addition{
	public:
		void calcadd();
};
class Subtraction{
	public:
		void calcsub();
};
class Multiplication{
	public:
		void calcmul();
};
class Division{
	public:
		void calcdiv();
};
int main (){
	do
	{
	cout << "SIMPLE CALCULATOR\n";
	cout << "Choose below the operator you want to use:" << endl;
	cout << "A.Addition" << endl;
	cout << "B.Subtraction" << endl;
	cout << "C.Multiplication" << endl;
	cout << "D.Division" << endl;
	cout << "T. Terminate the program" << endl;
	cin >> choices;
	if (choices == "A" || choices == "a")
	{
	Addition AdditionObj;
	AdditionObj.calcadd();
	}
	else if (choices == "B" || choices == "b")
	{
	Subtraction SubtractionObj;
	SubtractionObj.calcsub();
	}
	else if (choices == "C" || choices == "c")
	{
	Multiplication MultiplicationObj;
	MultiplicationObj.calcmul();
	}
	else if (choices == "D" || choices == "d")
	{
	Division DivisionObj;
	DivisionObj.calcdiv();
	}
	else if (choices == "T" || choices == "t")
	{
	exit (0);
	}
	else
	{
	cout << "Invalid input!!! Please any key to try again!" << endl;
	getch();
	main();
	}
	}
	while(choices == "Y" || choices == "y");
	exit (0);
	}
void Addition::calcadd()
{
	cout << "ADDITION MODULE\n";
	cout << "Enter first number: " << endl;
	cin >> numone;
	cout << "Enter second number: " << endl;
	cin >> numtwo;
	result = numone+numtwo;
	cout << "The sum is " << result << endl;
	cout << "Do you want to continue?" << endl;
	cin >> decision;
	if (decision == 'Y' || decision == 'y')
	{
	main();
	}
}
void Subtraction::calcsub()
{
	cout << "SUBTRACTION MODULE\n";
	cout << "Enter first number: " << endl;
	cin >> numone;
	cout << "Enter second number: " << endl;
	cin >> numtwo;
	result = numone-numtwo;
	cout << "The difference is " << result << endl;
	cout << "Do you want to continue?" << endl;
	cin >> decision;
	if (decision == 'Y' || decision == 'y')
	{
	main();
	}
}
void Multiplication::calcmul()
{
	cout << "MULTIPLICATION MODULE\n";
	cout << "Enter first number: " << endl;
	cin >> numone;
	cout << "Enter second number: " << endl;
	cin >> numtwo;
	result = numone*numtwo;
	cout << "The product is " << result << endl;
	cout << "Do you want to continue?" << endl;
	cin >> decision;
	if (decision == 'Y' || decision == 'y')
	{
	main();
	}
}
void Division::calcdiv()
{
	cout << "DIVISION MODULE\n";
	cout << "Enter first number: " << endl;
	cin >> numone;
	cout << "Enter second number: " << endl;
	cin >> numtwo;
	result = numone/numtwo;
	cout << "The quotient is " << result << endl;
	cout << "Do you want to continue?" << endl;
	cin >> decision;
	if (decision == 'Y' || decision == 'y')
	{
	main();
	}
}
