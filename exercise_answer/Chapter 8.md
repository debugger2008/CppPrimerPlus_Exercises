## 8.7 复习题

1.答案：代码量很小且需频繁调用的函数适合定义为内联函数。另外不能有循环体，不能有递归，否则会被拒绝内联。

2.a.答案：void song(const char * name, int times = 1);

  b.答案：不需要修改。
  
  c.答案：可以，但是要么和times参数一起提供默认值，如void song(const char * name = ”O.My Papa", int times = 1);要么把参数移到最右边，如void song(int times,const char * name = ”O.My Papa"）
  
3.答案：

```
void iquote(int a) //#1 type int parameter
{
  cout<<"\""<<a<<"\'"<<endl;
}

void iquote(double a) //#2 type double parameter
{
  cout<<"\""<<a<<"\'"<<endl;
}

void iquote(string a) //#3 type string parameter
{
  cout<<"\""<<a<<"\""<<endl;
}
```

4.a答案：
```
void Show(const box & a)
{
   using namespace std;
   cout << a.maker << endl;
   cout << a.height << endl;
   cout << a.width << endl;
   cout << a.length << endl;
   cout << a.volume << endl;
}
```
b答案：
```
void Show(const box & a)
{
   using namespace std;
   a.volume = a.height*a.width*a.length;
}
```

5.答案：
函数原型修改为void fill(std::array<double,Seasons> & pa); void show(std::array<double,Seasons> & da);
主函数修改部分：fill(expenses);
函数定义个性部分：
```
void fill(std::array<double,Seasons> & pa)
{
    using namespace std;
    for (size_t i = 0; i < Seasons; i++)
    {
        cout << "Enter " << Snames[i] << "expenses: ";
        cin >> pa[i];
    }
}

void show(std::array<double, Seasons> & da)
{
    using namespace std;
    double total = 0.0;
    cout << "\nEXPENSES\n";
    for (size_t i = 0; i < Seasons; i++)
    {
        cout << Snames[i] << ": $" << da[i] << endl;
        total += da[i];
    }
    cout << "Total Expense: " << total << endl; 
}
 ```
6.a答案：可以用函数默认参数完成，double mass(density,volume);double mass(density,volume=1);
   b答案：只能用函数重载完成，void repeat(string);
   c答案：只能用函数重载完成，int(int , int);average(double , double);
   d答案：两种都不行。
   
7.答案：
 ```
template<typename T>
T bigger(T a, T b)
{
    return a > b ? a : b; 
}
```
8.答案：
```
template <> box max(box b1, box b2)
{
    return b1.volume > b2.volume ? b1: b2; 
}
```
9.答案：<br>
v1 is type float <br> v2 is type float& <br> v3is type float$ (注意是两层括号) <br> v4 is type int  <br> v5 is type double （因为2.0是double，double与float的运算表达式是double)

