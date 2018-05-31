# baccode
#include "stdafx.h"
#include <iostream>
#include <fstream>

using namespace std;

int n, m, x, y,i,j;

int main()
{
	ifstream f("file.txt"), g("file2.txt");

	f >> n;
	g >> m;

	i = 1; j = 1;
	f >> x;
	g >> y;

	while (i <= n && j <= m)
	{
		if (x < y)
		{
			cout << x << " ";
			i++;
			f >> x;
		}
		else if (x > y)
		{
			cout << y << " ";
			j++;
			g >> y;
		}
		else
		{
			cout << x << " ";
			i++;
			j++;
			f >> x;
			g >> y;
		}
	}
	while (i <= n)
	{
		f >> x;
		i++;
		cout << x<<" ";
	}
	while (j <= m)
	{
		g >> y;
		j++;
		cout << y << " ";
	}

	cout << endl;
	system("PAUSE");
    return 0;
   }
