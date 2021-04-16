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
