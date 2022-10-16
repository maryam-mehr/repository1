# repository1
operator overload
#include<iostream>
using namespace std;
class Rectangle
{
	int length;
	int width;
public:
	void getvalues()
	{
		cout << "enter length" << endl;
		cin >> length;
		cout << "enter width" << endl;
		cin >> width;
	}
	void display(Rectangle& r)
	{
		cout << "length = " << length << endl;
		cout << "width = " << width << endl;
	}
	Rectangle()
	{
		length = 0;
		width = 0;
	}
	Rectangle(int a, int b)
	{
		length = a;
		width = b;
	}
	Rectangle operator+ (Rectangle const & a)
	{
		Rectangle result;
		result.length = a.length + length;
		result.width = a.width + width;
		return result;
	}
};
int main()

{
	Rectangle x;
	x.getvalues();
	Rectangle y;
	y.getvalues();
	Rectangle z = x + y;
	z.display(z);
}
