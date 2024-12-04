# Методичні вказівки до виконання лабораторної роботи
## Тема: Абстрактні класи та інтерфейси
## Мета: Навчитись використовувати абстрактні класи та інтерфейси

## Теоретичні відомості
Ознайомтеся з інформацією про абстрактні класи та інтерфейси


**Приклад використання абстрактних класів та інтерфейсів**

```csharp
using System;

namespace AbstractsANDInterfaces
{
    public abstract class Employee
    {
        //we can have fields and properties 
        //in the Abstract class
        protected String id;
        protected String lname;
        protected String fname;
        //properties
        public abstract String ID
        {
            get;   set;
        }

        public abstract String FirstName
        {
            get;   set;
        }

        public abstract String LastName
        {
            get;   set;
        }
        //completed methods
        public String Update()
        {
            return "Employee " + id + " " +
                      lname + " " + fname +
                      " updated";
        }
        //completed methods


        public String Add()
        {
            return "Employee " + id + " " +
                      lname + " " + fname +
                      " added";
        }
        //completed methods
        public String Delete()
        {
            return "Employee " + id + " " +
                      lname + " " + fname +
                      " deleted";
        }
        //completed methods
        public String Search()
        {
            return "Employee " + id + " " +
                      lname + " " + fname +
                      " found";
        }

        //abstract method that is different 
        //from Fulltime and Contractor
        //therefore i keep it uncompleted and 
        //let each implementation 
        //complete it the way they calculate the wage.
        public abstract String CalculateWage();
    }
}

//Приклад інтерфейсу
using System;
namespace AbstractsANDInterfaces
{
    public interface IEmployee
    {
        //cannot have fields. uncommenting 
        //will raise error!
        //        protected String id;
        //        protected String lname;
        //        protected String fname;

        //just signature of the properties 
        //and methods.
        //setting a rule or contract to be 
        //followed by implementations.
        String ID
        {
            get; set;
        }
        String FirstName
        {
            get;  set;
        }

        String LastName
        {
            get;   set;
        }

        // cannot have implementation
        // cannot have modifiers public 
        // etc all are assumed public
        // cannot have virtual
        String Update();
        String Add();
        String Delete();
        String Search();
        String CalculateWage();
    }
}


```


## Хід виконання:
1.	За основу візьміть попередню лабораторну, проаналізуйте ваші класи, виділіть загальні особливості і додайти абстрактний клас. В класах повинні бути присутні конструктори та деструктори.
2.	Також допишіть в ту саму програму інтерфес для ваших класів. Продемонструйте роботу інтерфейсів.
3.	Завантажити код із репозиторію. Інструкція як клонувати репозиторій написано тут https://www.youtube.com/watch?v=DdT4yODMUno.
4.	У Visual Studio дописати потрібний код для вирішення поставленого завдання. 
5.	Перевірити код на дотримання Code Convention C#:
 (https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions , https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/identifier-names )
6.	Перевірити на дотримання принципу інкапсуляції.
7.	Завантажити код програми на GitHub.
8.	Проконтролювати появу коментарів та зауважень щодо вашого виконання завдання у системі GitHub. За потреби внесіть корективи.
9.	Оформити звіт у гуглдокументі.

   
# Варіанти завдань для самостійної роботи:

## 1. Створити клас "Трикутник".
Створити відповідні методи:
- завдання координат вершин;
- виведення координат вершин на екран;
- обчислення площі.

Описати похідний від нього клас "Опуклий чотирикутник" з відповідними перевантаженими методами:
- завдання координат вершин;
- виведення координат вершин на екран;
- обчислення площі.

Створити об'єкти "трикутник" і "опуклий чотирикутник" та обчислити їх площі.

## 2. Створити клас "одновимірний вектор розмірності 4".
Створити відповідні методи:
- завдання елементів вектора;
- виведення вектора на екран;
- знаходження максимального елемента вектора.

Описати похідний від нього клас "матриця" розмірності 4х4 з відповідними перевантаженими методами:
- завдання елементів матриці;
- виведення матриці на екран;
- знаходження максимального елемента матриці.

Створити об'єкти класів "одновимірний вектор" та "матриця". Знайти максимальні елементи кожного об'єкта.

## 3. Описати клас "дробово-лінійна функція" виду $$\frac{a_1 x + a_0}{b_1 x + b_0}$$
Створити відповідні методи:
- завдання коефіцієнтів чисельника та знаменника;
- виведення коефіцієнтів на екран;
- знаходження значення в заданій точці $x_0$.

Створити похідний від нього клас "дробова функція $$\frac{a_2 x^2 + a_1 x + a_0}{b_2 x^2 + b_1 x + b_0}$$" з перевантаженими методами:
- завдання коефіцієнтів чисельника та знаменника;
- виведення коефіцієнтів на екран;
- знаходження значення в заданій точці $x_0$.

Створити об'єкти класів "дробово-лінійна функція" та "дробова" та обчислити їх значення у відповідній точці.

## 4. Описати клас "пряма" виду $$a_1 x + a_2 y + a_0 = 0$$ (тут $a_0, a_1, a_2$ - задані числа).

Створити відповідні методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- визначення, чи належить задана точка прямій.

Створити похідний клас "гіперплощина" виду
$$a_4 x_4 + a_3 x_3 + a_2 x_2 + a_1 x_1 + a_0 = 0$$
(тут $a_0, a_1, a_2, a_3, a_4$ - задані числа),
де $X = (x_1, x_2, x_3, x_4)$ - точка 4-вимірного простору.

Перевантажити відповідні методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- визначення, чи належить задана точка гіперплощині.

Створити об'єкти класів "пряма" та "гіперплощина". Визначити, чи належать введені користувачем точки створеним об'єктам.

## 5. Створити клас "круг $$(x_1 - b_1)^2 + (x_2 - b_2)^2 + (x_3 - b_3)^2 = R^2$$ "
Описати методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- визначення об’єму кулі.

Створити похідний клас „еліпсоїд $$\frac{(x_1  - b_1)^2}{a_1 ^2}+\frac{(x_2  - b_2)^2}{a_2 ^2}+\frac{(x_3  - b_3)^2}{a_3 ^2}=1$$”, де a_i,b_i ,i=1,3  – задані числа. Перевантажити відповідні методи:
- задання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- визначення об’єму еліпсоїда.
 	Створити об’єкти класів „куля” та „ еліпсоїд ”. Визначити об’єми кулі та еліпсоїда. 

## 6. Створити клас "двовимірна матриця A[3][3]".
Створити методи:
- завдання елементів матриці, використовуючи введення з клавіатури;
- завдання елементів матриці, використовуючи випадкові числа;
- знаходження мінімального елемента матриці.

Створити похідний клас "тривимірна матриця A[3][3][3]". Перевантажити відповідні методи:
- завдання елементів матриці, використовуючи введення з клавіатури;
- завдання елементів матриці, використовуючи випадкові числа;
- знаходження мінімального елемента матриці.

Створити об’єкти класів "двовимірна матриця" та "тривимірна матриця". Визначити мінімальні елементи всіх матриць.

## 7. Створити клас "півплощина $a_1 x_1 +a_2 x_2 \<= b$".
Створити відповідні методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- визначення, чи належить введена користувачем точка $X = (x_1, x_2)$ даній півплощині.

Створити похідний клас "півпростір", де $a_1 x_1 + a_2 x_2 + a_3 x_3  \leq b$ (тут  a_1, a_2, a_3$ - задані числа), $X = (x_1, x_2, x_3)$ - точка простору.

Перевантажити відповідні методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- визначення, чи належить введена користувачем точка $X = (x_1, x_2, x_3)$ даному півпростору.

Створити об’єкти класів "півпростір" та "півплощина". Визначити, чи належать введені користувачем точки півпростору та півплощині.

## 8. Створити клас "прямокутник $b_1 \leq x_1 \leq a_1 , b_2 \leq x_2 \leq a_2$ ".
Описати методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- визначення, чи належить введена користувачем точка заданому прямокутнику.

Створити похідний від нього клас "паралелепіпед $b_1 \leq x_1 \leq a_1 , b_2 \leq x_2 \leq a_2 , b_3 \leq x_3 \leq a_3$", де $a_i, b_i$, $i = 1, 3$ – задані числа.

Перевантажити відповідні методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- визначення, чи належить введена користувачем точка заданому паралелепіпеду.

Створити об’єкти класів "паралелепіпед" та "прямокутник". Визначити, чи належать введені користувачем точки вказаним об’єктам.

## 9. Створити клас "система рівнянь "
$$\begin{cases}
a_{11}x_{1} + a_{12}x_{2} = b_{1} \\
a_{21}x_{1} + a_{22}x_{2} = b_{2}
\end{cases}$$

 
 


Створити відповідні методи:
- завдання коефіцієнтів рівнянь та вільних членів;
- виведення системи рівнянь на екран;
- визначення, чи задовольняє введений користувачем вектор $X = (x_1, x_2)$ дану систему рівнянь.

Створити похідний від нього клас "система лінійних алгебраїчних рівнянь"

$$\begin{cases}
a_{11}x_{1} + a_{12}x_{2} + a_{13}x_{3} = b_{1} \\
a_{21}x_{1} + a_{22}x_{2} + a_{23}x_{3} = b_{2} \\
a_{31}x_{1} + a_{32}x_{2} + a_{33}x_{3} = b_{3}
\end{cases}$$

Перевантажити відповідні методи:
- завдання коефіцієнтів рівнянь та вільних членів;
- виведення СЛАР на екран;
- визначення, чи задовольняє введений користувачем вектор $(X = (x_1, x_2, x_3)$ даний СЛАР.

Створити об'єкти класів "система рівнянь $2 \times 2\$, "СЛАР $3 \times 3$". Визначити, чи задовольняють введені користувачем вектори створеним об'єктам "система рівнянь $2 \times 2$" та "СЛАР $3 \times 3$".

## 10. Описати клас "дріб $\frac{1}{a x}$".
Створити відповідні методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- обчислення значення відповідного дробу у введеній користувачем точці \(x\).

Створити похідний від нього клас - тригонометричний підхідний дріб виду

$$\frac{1}{a_1 x+\frac{1}{a_2 x+\frac{1}{a_3 x}}}, \quad i = 1,3, \quad задані числа, причому \quad a_i \neq 3$$

Перевантажити відповідні методи:
- завдання відповідних коефіцієнтів;
- виведення відповідних коефіцієнтів на екран;
- обчислення значення дробу у введеній користувачем точці.

Створити об'єкти класів "дріб" та "тригонометричний підхідний дріб". Обчислити значення дробів у заданих користувачем точках.

## 11. Описати клас "трикутник", який визначається координатами трьох точок на площині.
Створити відповідні методи:
- завдання координат трикутника;
- виведення координат трикутника на екран;
- обчислення площі трикутника.

Створити похідний від нього клас "тетраедр", який визначається координатами чотирьох точок на площині. Перевантажити відповідні методи.
- завдання координат вершин  тетраедр;
- виведення відповідних коефіцієнтів на екран;
- обчислення об'єму тетраедра.

Створити об’єкти класів „трикутник” та „ тетраедр”. Обчислити площу трикутника та об’єм тетраедра.

## 12. Описати клас „лінійна функція $$a_1 x + a_0$$ ”. 

Створити відповідні методи:
- задання коефіцієнтів лінійної функції;
- виведення відповідних коефіцієнтів на екран;
- обчислення значення лінійної функції в точці .
    
Створити похідний клас „многочлен $a_4 x^4 +a_3 x^3 +a_2 x^2 + a_1 x+a0$”, який визначається коефіцієнтами  $a_i$,i=0,4  з відповідними перевантаженими методами:
- задання коефіцієнтів многочлена;
- виведення відповідних коефіцієнтів на екран;
- обчислення значення многочлена в точці $x$.
Створити об’єкти класів „лінійна функція” та „многочлен”. Обчислити значення функцій у введеній користувачем точці.

## 13.  Дано клас „рівносторонній трикутник”. 

Створити відповідні методи:
- задання значення довжини сторони та кутів;
- знаходження інших характеристик трикутника: довжин сторін;
- обчислення периметра.
    
Створити похідний клас „трикутник”, який визначається довжиною однієї із сторін та значеннями прилеглих двох кутів з відповідними перевантаженими методами: 
- задання значення довжини сторони та двох кутів;
- знаходження інших характеристик трикутника: величини кутів та довжин сторін;
- обчислення периметра.
Створити об’єкти класів „рівносторонній трикутник” та „трикутник”. Знайти інші характеристики створених трикутників та їх периметри.

## 14. Описати клас „полярна система координат” та створити відповідні методи:

- задання координат в полярній системі координат;
- задання координат в декартовій системі;
- перетворення координат заданої точки з полярної системи в декартову;
- перетворення координат заданої точки з декартової системи в полярну.
    
Створити похідний клас „циліндрична система координат” і перевантажити відповідні методи:
- задання координат в циліндричній системі координат;
- задання координат в декартовій системі;
- перетворення координат заданої точки з циліндричної системи в декартову;
- перетворення координат заданої точки з декартової системи в циліндричну.
    
Створити об’єкти класів „циліндрична система координат” та „полярна система координат”. Перевести введені користувачем точки з циліндричної системи в декартову та з декартової в полярну систему.

## 15. Описати клас „еліпс $$\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$$ ”. Створити відповідні методи:

- задання коефіцієнтів;
- виведення коефіцієнтів на екран;
    
Описати похідний клас „крива другого порядку $$a_{11} x^2 + 2a_{12} xy+a_{22} y^2+b_1 x+b_2 y +c = 0$$” з відповідними перевантаженими методами:
- задання коефіцієнтів;
- виведення коефіцієнтів на екран;
- визначення чи належить задана точка (x,y) даній кривій другого порядку.
Створити об’єкт класу „еліпс” і визначити чи належить введена користувачем точка (x,y) даному еліпсу.

## 16. Створити клас „система двох векторів $$A=(a_1,a_2)$$ , $$B=(b_1,b_2)$$ ” і описати відповідні методи:

- задання координат векторів;
- виведення координат вектора на екран;
- визначення, чи система векторів A, B є лінійно незалежною.
    
Описати похідний клас „система 3-х векторів $$A=(a_1,a_2,a_3)$$ , $$B=(b_1,b_2,b_3)$$ , $$C=(c_1,c_2,c_3)$$” з відповідними перевантаженими методами:
- задання координат векторів;
- виведення координат вектора на екран;
- визначення, чи система векторів $$A,B,C$$ є лінійно незалежною.

Створити об’єкти класів „система 2-х векторів” та „система 3-х векторів”. Визначити чи система даних векторів не є лінійно залежними.

## 17 Описати клас „людина” який містить ім’я, прізвище, по-батькові, число, місяць, рік народження і описати відповідні методи:
- задання відповідних даних;
- визначення за поточною введеною датою віку людини;
- обчислення кількість зустрічань певної літери (літера вводиться користувачем) в прізвищі людини.

Описати похідний клас „студент”, що містить додаткове поле рік вступу до ВУЗу та спеціальність з відповідними перевантаженими методами:
- задання відповідних даних;
- визначення за поточною введеною датою віку студента;
- обчислення кількість зустрічань певної літери (літера вводиться користувачем) в прізвищі людини.

Створити об’єкти класів „людина” та „студент”. За поточною введеною датою визначити вік студента. Визначити кількість зустрічань введеної користувачем літери в прізвищі людини.

## 18 Дано клас „прямокутній трикутник”.
Створити відповідні методи:
- обчислення периметра.

Створити похідний клас „трикутник”, який визначається довжинами двох сторін та значенням кута між ними та  з відповідними перевантаженими методами:
- задання значення довжини сторони та двох кутів;
- знаходження інших характеристик трикутника: величини кутів та довжин сторін;
- обчислення периметра.

Створити об’єкти класів „прямокутній трикутник” та „трикутник”. Знайти інші характеристики створених трикутників та їх периметри. 

## 19 Описати клас „система двох лінійних нерівностей ”, створити відповідні методи:

$$\begin{cases}
a_{11}x_{1} + a_{12}x_{2} \leq b_{1} \\
a_{21}x_{1} + a_{22}x_{2} \leq b_{2}
\end{cases}$$

- задання коефіцієнтів відповідних нерівностей;
- виведення коефіцієнтів на екран;
- визначення, чи задовольняє введений користувачем вектор $$X=(x1, x2)$$ даній системі нерівностей.

Створити похідний клас „система трьох лінійних нерівностей

$$\begin{cases}
a_{11}x_{1} + a_{12}x_{2} + a_{13}x_{3} \leq b_{1} \\
a_{21}x_{1} + a_{22}x_{2} + a_{23}x_{3} \leq b_{2} \\
a_{31}x_{1} + a_{32}x_{2} + a_{33}x_{3} \leq b_{3}
\end{cases}$$

” і перевантажити відповідні методи:
- задання коефіцієнтів відповідних нерівностей;
- виведення коефіцієнтів на екран;
- визначення, чи задовольняє введений користувачем вектор $$X=(x_1,x_2,x_3)$$ даній системі нерівностей.

Створити об’єкт класу „система лінійних нерівностей” і визначити чи введена користувачем точка задовольняє даній системі.   

## 20 Описати клас „практикант”, який містить прізвище та ім’я практиканта; назву ВУЗу, в якому вчиться практикант. Описати відповідні методи: 
- задання вказаних даних;
- визначення чи прізвище є симетричним.

Створити похідний клас „працівник фірми” з відповідними перевантаженими методами, який також містить дату прийому на роботу в фірму; назву навчального закладу, який закінчив та посаду:
- задання вказаних даних;
- визначення стажу роботи на фірмі;
- визначення чи прізвище є симетричним.

Створити об’єкти класів „працівник фірми” та „практикант”. Для працівника визначити стаж його роботи на фірмі. Для практиканта визначити чи його прізвище є симетричним.

## 21 Описати клас „квадратне рівняння $$b_2x^2 +b_1x+b_0=0$$ ”, який містить: 
- методи задання коефіцієнтів  $$b2, b1, b1$$ та метод виведення їх на екран;
- метод визначення, чи задовільняє введене користувачем число даному рівнянню.

Поповнити даний клас методом пошуку коренів квадратного рівняння.	

Створити похідний клас „кубічне рівняння $$a_3x^3+a_2x^2+a_1x+a_0=0$$ ”. Перевантажити відповідні методи:
- методи задання коефіцієнтів $$a_3,a_2,a_1,a_0$$ та метод виведення їх на екран;
- метод визначення, чи задовільняє введене користувачем число $$x$$ даному рівнянню.

Створити об’єкт класів „квадратне рівняння” та „кубічне рівняння”. Знайти корені квадратного рівняння. Визначити, чи задовільняє введене користувачем число $x$ кубічному рівнянню.

## 22 Створити клас „коло  $$(x-x_0)^2+(y-y_0)^2=R^2$$  ” і створити відповідні методи: 
- задання координат $$(x_0, y_0 )$$ центру кола та його радіусу R, а також виведення цих даних на екран;
- визначення довжини кола. 

Створити похідний клас „сфера $$(x-x_0)^2+(y-y_0)^2+(z-z_0)^2=R^2$$ ”. Перевантажити відповідні методи:
- задання координат $$(x_0, y_0, z_0 )$$ центру сфери та її радіусу R, а також виведення цих даних на екран;
- визначення площі поверхні сфери. 

Створити об’єкти класів „коло  $$(x-x_0)^2+(y-y_0)^2=R^2$$ ” та „сфера сфера $$(x-x_0)^2+(y-y_0)^2+(z-z_0)^2=R^2$$”. Визначити довжину кола та площу поверхні сфери.


## 23. Описати клас „рухома матеріальна точка”, яка ріхається по прямій і координата її визначається як $$x=x_0+a_1 sin(t), y=0,z=0$$ .  
Описати відповідні методи:
- задання початкового положення точки x0;
- задання коефіцієнтів a1 та виведення їх на екран;
- визначення координат точки в заданий момент часу t.  

Створити похідний клас „рухома матеріальна точка $$(x,y,z)$$ ”, координати якої визначаються як $$x=x_0+a_1 sin(t), y=y_0+a_2 cos(t),z=z_0+a_3t^2$$ . Перевантажити відповідні методи:
- задання початкового положення точки $$(x_0,y_0,z_0)$$ ;
- задання коефіцієнтів $$a_3,a_2,a_1$$ та виведення їх на екран;
- визначення координат точки в заданий момент часу $t$ .  

Створити об’єкти класів „рухома матеріальна точка $x$ ” та „рухома матеріальна точка $$(x,y,z)$$ ” і визначити їх положення у введений користувачем момент часу $t$.

## 24. Задано клас „коло в просторі”, який буде характеризуватись центром та радіусом.  
Описати метод:
- задання вказаних даних та виведення їх на екран;
- метод визначення довжини кола.  

Описати похідний клас „конус”, який характеризується координатами вершини, координатами центру основи та твірною. Перевантажити відповідні методи:
- задання вказаних даних та виведення їх на екран;
- метод визначення бічної поверхні конуса;
- метод визначення радіуса основи конуса.  

Створити об’єкти класів „коло в просторі” та „конус”. Визначити радіус основи конуса. Визначити довжину кола.

## 25. Описати клас „перетворення площини 

$$\begin{cases}
x' = a_{11}x_{} + a_{12}y_{}+a_{13}  \\
y' = a_{21}x_{} + a_{22}y_{}+a_{23}
\end{cases}$$

” та створити відповідні методи:
- задання коефіцієнтів перетворення;
- виведення коефіцієнтів перетворення на екран;
- визначення образу заданої точки (x, y).  

Описати похідний клас „перетворення простору

$$\begin{cases}
x'= a_{11}x + a_{12}y + a_{13}z +a_{14}  \\
y'= a_{21}x + a_{22}y + a_{23}z +a_{24} \\
z'= a_{31}x + a_{32}y + a_{33}z +a_{34}
\end{cases}$$

” з відповідними перевантаженими методами:
- задання коефіцієнтів перетворення;
- виведення коефіцієнтів перетворення на екран;
- визначення образу заданої точки $$(x,y,z)$$ .  

Створити об’єкт класу „перетворення площини” і знайти образ введеної користувачем точки.


## Контрольні запитання
Що таке абстрактний клас?
Чи допускають мови програмування С++ (С#) створення об’єктів абстрактного класу?
Що таке інтерфейс?
Яка різниця між інтерфейсом та абстрактним класом?
Коли потрібно використовувати інтерфейс замість абстрактного класу?
