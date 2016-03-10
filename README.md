# -
用于记录自己平时所学所想
初次发博，四册运算的随机生成代码以及运行结果：
//邵文正 20142894  2016.3.7
#include<iostream>
using namespace std;
int random()
{
	return(rand()%100);
}
char Fuhao()
{
	int a;
	a = rand() % 4;
	if (a == 1)
	{
		return '+';
	}
	if (a == 2)
	{
		return '-';
	}
	if (a == 3)
	{
		return'*';
	}
	else
	{
		return'/';
	}
}
void Jiafenshu()
{
	int x, y;
	m:y = rand() % 10;
	if (y == 0)
	{
		goto m;
	}
	x = rand() % 100;
	cout <<"("<< x << "/" << y<<")" ;
}
void main()
{
	int a, b;
	
	cout << "以下是30个四则运算不包含假分数\n" << endl;
	for (int i = 0; i < 30; i++)
	{
		x:a = random();
		b = random();
		Fuhao();
		if (Fuhao() == '/' || b == 0)
		{
			goto x;
		}
		cout << a << Fuhao() << b << "=   " << endl;
	}
	cout << "以下是假分数的运算30个：\n" << endl;
	for (int i = 0; i < 30; i++)
	{
		Jiafenshu();
		cout << Fuhao(); 
		Jiafenshu();
		cout <<"=  "<< endl;
	}
	  
}

