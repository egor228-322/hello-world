#include "stdafx.h"
#include <iostream> 
#include <math.h> 
using namespace std;
const int n = 11;
int main()
{
	setlocale(0, "Rus");
	int i;
	float x[n], y[n], sX = 0, sY = 0, arr[n], sP = 0, q[n], sQ = 0, a, b;
	cout << "Введите x: \n";
	for (i = 0; i < n; i++)
		cin >> x[i];

	cout << "Введите y: \n";
	for (i = 0; i < n; i++)
		cin >> y[i];

	for (i = 0; i < n; i++)
		sX += x[i];

	for (i = 0; i < n; i++)
		sY += y[i];

	for (i = 0; i < n; i++)
	{
		arr[i] = 0;
		arr[i] = x[i] * y[i];
	}
	for (i = 0; i < n; i++)
		sP += arr[i];

	for (i = 0; i < n; i++)
	{
		q[i] = 0;
		q[i] = x[i] * x[i];
	}

	for (i = 0; i < n; i++)
		sQ += q[i];

	a = (n*sP - sX * sY) / (n*sQ - pow(sX, 2));
	cout << "a = " << a << endl;
	b = (sY -(a * sX)) / n;
	cout << "b = " << b << endl;
	system("pause");
	return 0;
}

