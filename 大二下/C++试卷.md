
### 一、单项选择题（共 20 小题，每小题 2 分，共 40 分）

1. 在 C++ 中使用流进行输入输出，下列哪个对象不是系统自动打开的。
    
    A. cerr
    
    B. cin
    
    C. cout
    
    D. cfile
    
2. 所谓数据封装就是将一组数据和与这组数据相关的操作组装在一起，形成一个实体。这个实体就是
    
    A. 类
    
    B. 对象
    
    C. 函数体
    
    D. 数据块
    
3. `int Fun(int, int);` 不可与下列哪个函数构成重载
    
    A. `int Fun(int, int, int);`
    
    B. `float Fun(int, int);`
    
    C. `float Fun(float, float);`
    
    D. `float Fun(int, float);`
    
4. 函数的形参是
    
    A. 全局变量
    
    B. 局部变量
    
    C. 静态变量
    
    D. 寄存器变量
    
5. 下面函数中能够声明为虚函数的是
    
    A. 构造函数
    
    B. 析构函数
    
    C. 友员函数
    
    D. 静态成员函数
    
6. 下列关于 new 运算符的描述中错误的是
    
    A. new 运算符可以用来动态创建对象和对象数组
    
    B. 若内存分配失败则返回一个空指针
    
    C. new 运算符为对象分配存储空间时需调用类的构造函数
    
    D. new 运算符创建数组时必须指定数组初值
    
7. 类 B 是类 A 的公有派生类，类 A 和类 B 中都定义了成员函数 `void mem_func()`。下面程序段中，`p->mem_func()` 将调用哪个函数？
    
    ```C++
    B Bobj;
    A *p = &Bobj;
    p->mem_func();
    ```
    
    A. 调用类 A 中的函数 `mem_func()`
    
    B. 调用类 B 中的函数 `mem_func()`
    
    C. 根据 p 指向的对象的类型决定调用哪个类中定义的函数 `mem_func()`
    
    D. 既调用类 A 中的函数，也调用类 B 中的函数
    
8. 要求指针 p 既不可修改其本身内容，也不可修改其所指向的内容，下面定义正确的是
    
    A. `const char *p = "ABCD";`
    
    B. `char * const p = "ABCD";`
    
    C. `char const *p = "ABCD";`
    
    D. `const char * const p = "ABCD";`
    
9. 下面程序的错误语句中错误原因为二义性错误的语句应该是
    
    ```C++
    struct Y;
    struct X {
        int I;
        X(int);
        X operator+(Y);
    };
    struct Y {
        int I;
        Y(X);
        Y operator+(X);
        operator int();
    };
    int main() {
        X x = 1;
        Y y = x;
        int ret = x + 10;  // 语句 A
        ret = y + 10;      // 语句 B
        ret = x + y;       // 语句 C
        ret = X * X;       // 语句 D
    }
    ```
    
10. 下列关于友员的描述中正确的是
    
    A. 若类 A 是类 B 的友员，则类 B 也是类 A 的友员
    
    B. 若类 B 是类 A 的友员且类 C 是类 B 的友员，则类 C 也是类 A 的友员
    
    C. 基类的友员也是派生类的友员
    
    D. 派生类的友员只能访问基类的公有成员
    
11. 所谓多态性是指
    
    A. 不同的对象调用不同名称的函数
    
    B. 同一对象调用不同名称的函数
    
    C. 不同对象调用相同名称的函数，函数的具体实现不同
    
    D. 不同对象调用相同名称的函数，函数的具体实现相同
    
12. 对于抽象类，下列描述正确的是
    
    A. 可以定义抽象类的对象
    
    B. 可以定义指向抽象类对象的指针
    
    C. 抽象类对象可以作为函数的形参和返回值使用
    
    D. 抽象类的派生类不再是抽象类
    
13. 关于运算符重载，下列说法正确的是
    
    A. 所有的运算符都可以重载。
    
    B. 通过重载，可以使运算符应用于自定义的数据类型。
    
    C. 通过重载，可以创造原来没有的运算符。
    
    D. 通过重载，可以改变运算符的优先级。
    
14. 已知：`int fun(int &a), m = 10;` 下列调用 `fun()` 函数的语句中，正确的是
    
    A. `fun(&m);`
    
    B. `fun(m * 3);`
    
    C. `fun(m);`
    
    D. `fun(m++);`
    
15. 假设 OneClass 为一个类，则该类的拷贝构造函数的声明语句为
    
    A. `OneClass(OneClass p);`
    
    B. `OneClass& (OneClass p);`
    
    C. `OneClass(OneClass &p);`
    
    D. `OneClass(OneClass *p);`
    
16. 复数类及其对象定义如下：
    
    ```C++
    class Complex {
        double real, image;
    public:
        Complex(double r = 0, double i = 0) { real = r; image = i; }
        Complex(Complex &c) { real = c.real; image = c.image; }
    };
    Complex c1;       // A 行
    Complex c2(3,5);  // B 行
    Complex c3(c2);   // C 行
    c2 = c1;          // D 行
    ```
    
    下列说法中正确的是
    
    A. C 行和 D 行均调用了拷贝构造函数
    
    B. 仅有 C 行调用了拷贝构造函数
    
    C. 仅有 B 行调用了拷贝构造函数
    
    D. 仅有 A 行调用了拷贝构造函数
    
17. 语句 `typedef double (* DAP) [10];` 中，DAP 是
    
    A. 数据类型名
    
    B. 数组型变量名
    
    C. 指针型变量名
    
    D. 数组指针型变量名
    
18. 关于类的静态成员，下面描述错误的是
    
    A. 静态成员函数不能声明为虚函数
    
    B. 静态成员是类的成员
    
    C. 只有在创建类的对象之后，静态成员才存在
    
    D. 静态成员函数不能直接访问非静态成员
    
19. 下列带缺省值参数的函数原型说明中，正确的说明是
    
    A. `int Func(int x, int y = 2, int z = 3);`
    
    B. `int Func(int = 1, int y, int z = 3);`
    
    C. `int Func(int x, int y = 2, int z);`
    
    D. `int Func(int x = 1, int y = 2, int z);`
    
20. 若有如下类定义：
    
    ```C++
    class MyClass {
    public:
        MyClass() { cout << '*'; }
    };
    ```
    
    则执行语句 `MyClass obj[2], *p[2];` 之后程序的输出结果是
    
    A. `*`
    
    B.
    
    C. `***`
    
    D. `****`
    

### 二、填空题（共 10 小题，每小题 2 分，共 20 分）

1. 经过私有派生后，基类的公有和保护成员在派生类中都将成为私有成员。作为私有派生的补充，C++通过 `___________` 可调整基类公有和保护成员在派生类中的访问权限。
    
2. 类的构造函数的特点包括：函数名与 `___________` 同名，没有返回值并且由系统自动调用。
    
3. 在下面 shape 抽象类的声明中加入纯虚函数 `void draw()` 的声明：
    
    ```C++
    class shape {
        int x;
        int y;
    public:
        ___________________________;
        void move(int mx, int my) { x = mx; y = my; }
    };
    ```
    
4. 类 A 的对象的 `this` 指针的数据类型为 `___________`。
    
5. 定义内联函数时需在函数原型前冠以保留字 `___________`。
    
6. 在下面 three_d 类的声明中加入用成员函数重载后缀自加运算符 (++) 的函数声明：
    
    ```C++
    class three_d {
        int x, y, z;
    public:
        ___________________________; // 用成员函数重载后缀“++”的函数声明
        void show();
        void assign(int mx, int my, int mz);
    };
    ```
    
7. 假设 Complex 类用成员函数重载了 ++ 运算符和 * 运算符。若 obj1 和 obj2 分别为 Complex 类的对象，则表达式 `++obj1 * obj2` 的显示表示形式为 `___________`。
    
8. 成员函数和静态成员函数的主要区别是 `___________`。
    
9. 若类 Sample 中只有两个数据成员：`const float f` 和 `int &ri`。则 Sample 类构造函数应定义为 `___________`。
    
10. 当派生类的多个基类又拥有一个公共基类时，可将该公共基类声明为 `___________` 来避免访问公共基类成员时产生的二义性。
    

### 三、程序分析题（共 5 小题，每小题 4分，共 20 分）

1. 阅读下列程序，写出相应的输出结果：

    ```C++
    #include <iostream>
    using namespace std;
    class Counter {
    public:
        Counter(int XX = 0, int yy = 0) { X = XX; Y = yy; count++; }
        Counter(Counter & cobj) { X = cobj.X; Y = cobj.Y; count++; }
        ~Counter() { count--; }
        static void print() { cout << "Number of the objects is " << count << endl; }
    private:
        int X, Y;
    };
    static int count;
    int Counter::count = 0;
    int main() {
        Counter::print();
        Counter A;
        Counter B = A;
        Counter *p = new Counter;
        Counter::print();
        delete p;
        Counter::print();
        return 0;
    }
    ```
    
    **答：**
    
    Number of the objects is 0
    
    Number of the objects is 3
    
    Number of the objects is 2
    
2. 阅读下列程序，写出相应的输出结果：

    ```C++
    #include <iostream>
    using namespace std;
    class A {
    public: 
        A() { cout << "class A" << endl; }
    };
    class B : public A {
    public: 
        B() { cout << "class B" << endl; }
    };
    class C : public A {
    public: 
        C() { cout << "class C" << endl; }
    };
    class D : public B, public C {
    public: 
        D() { cout << "class D" << endl; }
    };
    int main() { 
        D dd; 
    }
    ```
    
    **答：**
    
    class A
    
    class B
    
    class A
    
    class C
    
    class D
    
3. 阅读下列程序，写出相应的输出结果：
    
    ```C++
    #include <iostream>
    using namespace std;
    int a[] = {1, 3, 5, 7, 9};
    int *p[] = {a, a + 1, a + 2, a + 3, a + 4};
    void main() {
        cout << a[4] << *(a + 2) << *p[1] << endl;
        cout << **(p + 1) + a[2] << *(p + 4) - *(p + 0) << **(a + 3) % a[4];
    }
    ```
    
    **答：**
    
    953
    
    847
    
4. 阅读下列程序，写出相应的输出结果：
    
    ```C++
    #include <iostream>
    using namespace std;
    int & get_var(int * pint) {
        return * pint;
    }
    void main() { 
        int anInt = 10;
        int otherInt;
        otherInt = get_var(&anInt) * 12;
        get_var(&anInt) = 200;
        cout << otherInt << '\t' << anInt << endl;
    }
    ```
    
    **答：**
    
    120 200
    
5. 阅读下列程序，写出相应的输出结果：
    
    ```C++
    #include <iostream>
    using namespace std;
    int m = 10;
    int main() {
        int m = 20;
        {
            int m = 30;
            cout << "we are in the inner block \n";
            cout << "m=" << m << "\n";
            cout << "::m=" << ::m << "\n";
        }
        cout << "\n We are in the outer block \n";
        cout << "m=" << m << "\n";
        cout << "::m=" << ::m << "\n";
        return 0;
    }
    ```
    
    **答：**
    
    we are in the inner block
    
    m=30
    
    ::m=10
    
    We are in the outer block
    
    m=20
    
    ::m=10
    

### 四、程序填空题（共 5 小题，每空 2 分，共 20 分）

1. 请将程序补充完整，使程序的输出为：
    Derived A
    Derived B
    ```C++
    #include <iostream>
    using namespace std;
    class Base { 
    public:
        Base(int i) : val(i) {}
        virtual void Show() { cout << "Base" << endl; };
    protected:
        int val;
    };
    class DerivedA : public Base { 
    public:
        DerivedA(int i) : Base(i) {}
        void Show() { cout << "Derived A" << endl; }
    };
    class DerivedB : public Base { 
    public:
        DerivedB(int i) : Base(i) {}
        void Show() { cout << "Derived B" << endl; }
    };
    void fun(Base & n) { 
        n.Show(); 
    }
    int main() {
        DerivedA d(50);
        fun(d);
        DerivedB h(16);
        fun(h);
        return 0;
    }
    ```
    
2. 请将程序补充完整，使程序的输出为：`*******123 123.45`
    
    ```C++
    #include <iostream>
    using namespace std;
    int main() {
        cout.fill('*');
        cout.width(10);
        cout << 123 << ' ' << 123.45 << endl;
        return 0;
    }
    ```
    
3. 完成下面程序填空：
    
    ```C++
    class Array {
        int size;
        int * p;
    public:
        Array(int s) : size(s) {
            p = new int[size]; // 为有size个int型元素的数组动态分配存储空间
                               // 并把首地址返回给指针p
        }
        ~Array() { delete [] p; }
    };
    ```
    
1. 请将程序补充完整，使程序的输出为：`0.6`
    ```C++
    class Rational { 
    public:
        Rational(long n = 0, long d = 1) : Numerator(n), Denominator(d) {};
        operator double() // 类型转换函数，把 Rational 类对象转换成 double 型变量
        { return double(Numerator) / double(Denominator); }
    private:
        long Numerator, Denominator;
    };
    void display(double d) { 
        cout << d << endl; 
    }
    int main() { 
        Rational obj(3, 5);
        display(obj);
        return 0;
    }
    ```
    
2. 在下列程序的空格处填上适当的字句，使输出为：`0,2,10`。
    
    ```C++
    #include <iostream>
    #include <cmath>
    using namespace std;
    class Magic {
        double x;
    public:
        Magic(double d = 0.00) : x(fabs(d)) {}
        Magic operator+() {
            // 补充重载逻辑
            return *this; 
        }
    };
    // 补充流插入运算符重载
    ostream& operator<<(ostream & stream, Magic & c) {
        stream << c.x;
        return stream;
    }
    void main() {
        Magic ma;
        cout << ma << "," << Magic(2) << "," << ma + Magic(-6) + Magic(-8) << endl;
    }
    ```