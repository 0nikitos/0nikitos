

#include <iostream>
#include <stdlib.h>
#include <math.h>
using namespace std;

class Fraction
{
    int num, denum;

    

public:
    Fraction(int ch, int zn) {
        num = ch;
        denum = zn;
    }

    Fraction()
    {
        num = 0;
        denum = 0;
        
    }
    
    
    void  input()
    {
        
        cin >> num;
      
        cin >> denum;

    }
    void show() {
        cout << num << "/ " << denum << endl;
        
    }

   
    Fraction operator+( Fraction c)
    {
        int ch =num * c.denum + denum * c.num;
        int zn = denum * c.denum;
        return  c;
            
    }

  

    Fraction operator-(Fraction c)
    {
        int ch = num * c.denum - denum * c.num;
        int zn = denum * c.denum;
        return c;
    }

    Fraction operator*(Fraction c)
    {
        int ch = num * c.num;
        int zn = denum * c.denum;
        return c;
    }
    Fraction operator/(Fraction c)
    {
        int ch = num * c.denum;
        int zn = denum * c.num;
        return c;
    }

   
   
};


int main()
{
    
        setlocale(LC_ALL, "Russian");
       
        cout << "Дроби \n"
            " 1 - Ввод данных \n 2 - Сложение \n 3 - Вычитание \n 4 - Умножение\n"
            " 5 -Деление \n 6 - Сравнение \n 7 - Показать дробь" << endl;
        Fraction a,b,first;
        

        cout << "Введите дробь\n";
        a.input();

        cout << "Введите дробь\n";
        b.input();
        
        char Control;
        cout << ">";
        cin >> Control;


        switch (Control)
        {

        case '1':
            first=a+b;
            cout << ">";
            cin >> Control;
        case '2':
            first.operator-(b);
            cout << ">";
            
            cin >> Control;
            
        case '3':
            first.operator*(b);
            cout << ">";
            cin >> Control;
        case '4':
            first= a/b;
            cout << ">";
            cin >> Control;
            first.show();

       
        
        case '7':
            a.show();
            b.show();
            cout << ">";
            cin >> Control;
        }

        return 0;
    }
