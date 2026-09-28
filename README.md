
#include<bits/stdc++.h>
using namespace std;

class Shopping
{
public:
    int price,quantity;

    int calculate(int a,int b)
    {
        price=a;
        quantity=b;

        cout<<"Product Cost: "<<quantity*price<<endl;
        return quantity*price;
    }

    double calculate(float a,int b)
    {
        price=a;
        quantity=b;

        cout<<"Product Cost: "<<quantity*price<<endl;
        return quantity*price;
    }

    void calculate(int a,double b,int c)
    {
        double product1=a-(a*c/100.0);
        double product2=b-(b*c/100.0);

        double total=a+b;
        double finalPrice=product1+product2;

        cout<<"Total Price: "<<total<<endl;
        cout<<"Final Price: "<<finalPrice<<endl;
    }
};

int main()
{
    Shopping ob1;

    int p1=ob1.calculate(100,3);
    double p2=ob1.calculate(200.33f,3);

    ob1.calculate(p1,p2,5);

    return 0;
}
