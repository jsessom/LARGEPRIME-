# LARGEPRIME-
TRIES TO FIND LARGEST PRIME NUMBER
#include "stdafx.h"
#include <iostream>
#include <fstream>
#include <chrono>

using namespace std;
using namespace std::chrono;

bool is_prime(long long int n)
{
	if (n <= 1)
		return false;

	if (n <= 3)
		return true;

	if (n % 2 == 0 || n % 3 == 0)
		return false;

	for (int i = 5; i * i <= n; i = i + 6)
	{
		if (n % i == 0 || n % (i + 2) == 0)
		{
			return false;
		}
		return true;
	}

}



int main()
{

	long long int num;
	


	cout << "Please enter in an number or 0 to exit." << endl;
	cin >> num;
	
	

		is_prime(num) ? cout << "Prime\t "<< num<<endl : cout << "Not Prime\n";
		

	
	
	

	return 0;
}
