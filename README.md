#include <iostream>
#include <ctime>

using namespace std;

int main()
{
	srand(time(NULL)); 
	int n = 0;
	cin >> n;
	int **a = new int*[n];
	double k;
	int w;
	double g;
	for (int i = 0; i < n; i++)
	{
		a[i] = new int[n];
	}
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			a[i][j] = rand() % 3;
		
			if (a[i][j] == 2) {
				k++;
			}
			if (i == n & k > g) {
				g = k;
				//тут каким то образом должно оттодвигать все строки вниз на 1 освобождая место для этой строки и вставлять её туда
			}
			cout << a[i][j] << " ";
		}
	

		cout << endl; //
	}
	// Удаление массива
	for (int i = 0; i < n; i++)
	{
		delete[]a[i]; // Удаляем каждый элемент
	}
	delete[] a; // А потом массив
	return 0;
}
