1. 
```c#
using System;
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix un valor.
    //Postcon: L'usuari sap si el valor es natural.
    public class Activitats
    {
        public static void Comprovar(int num)
        {
            Console.WriteLine(num > 0 ? "It's Natural" : "It's not Natural");
        }
        public static void Main()
        {
            const string MSG1 = "Put a number and i will tell you if it's natural:";
            const string ERROR = "The format of the number is incorrect";
            int num;
            Console.WriteLine(MSG1);
            try
            {
                num = int.Parse(Console.ReadLine());
                Comprovar(num);
            }
            catch (Exception)
            {
                Console.WriteLine(ERROR);
            }
        }

    }
}
```
2. 
```c#
using System;
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix dos numeros
    //Postcon: L'usuari obte el primer valor elevat pel segon.
    public class Activitats
    {
        public static int Elevate(int num1,int num2)
        {
            num1 = (int)Math.Pow(num1, num2); //para que usar un metodo para usar otro metodo?
            return num1;
        }
        public static void Main()
        {
            const string MSG1 = "Put two numbers and i will elevate them";
            const string ERROR = "The format of the number is incorrect";
            int num, num2, result;
            Console.WriteLine(MSG1);
            try
            {
                num = int.Parse(Console.ReadLine());
                num2 = int.Parse(Console.ReadLine());
                result = Elevate(num, num2);
                Console.WriteLine(result);
            }
            catch (Exception)
            {
                Console.WriteLine(ERROR);
            }
        }

    }
}
```
3. 
```c#
using System;
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix un valor.
    //Postcon: L'usuari sap si el valor es negatiu.
    public class Activitats
    {
        public static void Comprovar(int num)
        {
            Console.WriteLine(num < 0 ? "It's Negative" : "It's not Negative");
        }
        public static void Main()
        {
            const string MSG1 = "Put a number and i will tell you if it's negative:";
            const string ERROR = "The format of the number is incorrect";
            int num;
            Console.WriteLine(MSG1);
            try
            {
                num = int.Parse(Console.ReadLine());
                Comprovar(num);
            }
            catch (Exception)
            {
                Console.WriteLine(ERROR);
            }
        }

    }
}
```
4. 
```c#
using System;
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix un valor.
    //Postcon: L'usuari sap si el valor es negatiu.
    public class Activitats
    {
        public static bool Comprovar(int num)
        {
            return num < 100&&num>0;
        }
        public static void Main()
        {
            const string MSG1 = "Put a number and i will tell you if it's beetween 0 and 100:";
            const string ERROR = "The format of the number is incorrect";
            int num;
            Console.WriteLine(MSG1);
            try
            {
                num = int.Parse(Console.ReadLine());
                Console.WriteLine(Comprovar(num)? "It's in Range" : "It's not in Range");
            }
            catch (Exception)
            {
                Console.WriteLine(ERROR);
            }
        }
    }
}
```
v2:
```c#
using System;
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix un valor.
    //Postcon: L'usuari sap si el valor es negatiu.
    public class Activitats
    {
        public static bool Comprovar(int num)
        {
            return num < 100 && num > 0;
        }
        public static bool Comprovar(int num, int min, int max)
        {
            return num < max && num > min;
        }
        public static void Main()
        {
            const string Msg1 = "Put a number and i will tell you if it's beetween 0 and 100:";
            const string Msg2 = "It's in Range";
            const string Msg3 = "It's not in Range";
            const string Msg4 = "Write the minimum";
            const string Msg5 = "Write the maximum";
            const string Error = "The format of the number is incorrect";
            int num, min, max;
            Console.WriteLine(Msg1);
            try
            {
                num = int.Parse(Console.ReadLine());
                Console.WriteLine(Msg4);
                min= int.Parse(Console.ReadLine());
                Console.WriteLine(Msg5);
                max= int.Parse(Console.ReadLine());
                Console.WriteLine(Comprovar(num, min, max) ? Msg2 : Msg3);
            }
            catch (Exception)
            {
                Console.WriteLine(Error);
            }
        }
    }
}
```
5. 
```c#
using System;
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix un valor.
    //Postcon: L'usuari sap si el valor es natural.
    public class Activitats
    {
        public static bool Comprovar()
        {
            int num;
            int attempt = 0;
            do
            {
                num = int.Parse(Console.ReadLine());
                attempt++;
            }
            while (num<=0&&attempt<3);
            if (num > 0 && attempt <= 3)
            {
                return true;
            }
            else
            {
                return false;
            }
        }
        public static void Main()
        {
            const string MSG1 = "Put a number and i will tell you if it's natural:";
            const string ERROR = "The format of the number is incorrect";
            bool result;
            Console.WriteLine(MSG1);
            try
            {
                result=Comprovar();
                Console.WriteLine(result ? "Good job" : "You lose");
            }
            catch (Exception)
            {
                Console.WriteLine(ERROR);
            }
        }
    }
}
```
6. 
```c#
using System;
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix un valor.
    //Postcon: L'usuari sap si el valor es natural.
    public class Activitats
    {
        public static int Absolut(int num)
        {
            if (num < 0)
            {
                num=-num;
            }
            return num;
        }
        public static void Main()
        {
            const string MSG1 = "Put a number and i will show his absolute value:";
            const string MSG2 = "The absolute value is: {0}";
            const string ERROR = "The format of the number is incorrect";
            int num;
            Console.WriteLine(MSG1);
            try
            {
                num = int.Parse(Console.ReadLine());
                num=Absolut(num);
                Console.WriteLine(MSG2,num);
            }
            catch (Exception)
            {
                Console.WriteLine(ERROR);
            }
        }
    }
}
```
7. 
```c#
using System;
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix un text.
    //Postcon: L'usuari rep el text en minuscules o majuscules.
    public class Activitats
    {
        public static string Change(string text)
        {
            if(text==text.ToUpper())
            {
                text=text.ToLower();
            }
            else if(text==text.ToLower())
            {
                text=text.ToUpper();
            }
            return text;
        }
        public static void Main()
        {
            const string MSG1 = "Put a text and i will change his letters:";
            const string MSG2 = "The text is now: {0}";
            const string ERROR = "The format of the number is incorrect";
            string text;
            Console.WriteLine(MSG1);
            try
            {
                text = Console.ReadLine();
                text=Change(text);
                Console.WriteLine(MSG2,text);
            }
            catch (Exception)
            {
                Console.WriteLine(ERROR);
            }
        }
    }
}
```
8. 
```c#
using System;
using LlibreriaSergi; //la llibreria es el projecte de C:\Users\isard\source\repos\LibreriaActivitatsC#SergiAlbalat
namespace ActivitatsProgramacio
{
    //Precon: L'usuari dos valors.
    //Postcon: L'usuari rep els valors intercanviats
    public class Activitats
    { 
        public static void Main()
        {
            const string Msg1 = "Put two numbers and i will change them.";
            const string Msg2 = "The first num is {0} and the second is {1}";
            const string Error = "The format of the number is incorrect";
            int num1, num2;
            Console.WriteLine(Msg1);
            try
            {
                num1 = int.Parse(Console.ReadLine());
                num2= int.Parse(Console.ReadLine());
                Utils.Intercanviar(ref num1, ref num2);
                Console.WriteLine(Msg2, num1, num2);
            }
            catch (Exception)
            {
                Console.WriteLine(Error);
            }
        }
    }
}
```
9. 
```c#
using System;
using LlibreriaSergi; //la llibreria es el projecte de C:\Users\isard\source\repos\LibreriaActivitatsC#SergiAlbalat
namespace ActivitatsProgramacio
{
    //Precon: L'usuari dos valors.
    //Postcon: L'usuari rep els valors intercanviats
    public class Activitats
    {
        public static void Main()
        {
            const string Msg1 = "Write a number and i will tell you how many digits does it have, the sum of all the evens and the sum of all the ods.";
            const string Msg2 = "The number have {0} digits.";
            const string Msg3 = "The sum of the evens is: {0}";
            const string Msg4 = "The sum of the ods is: {0}";
            const string Error = "The format of the number is incorrect";
            int num, evens=0, ods=0, digits;
            Console.WriteLine(Msg1);
            try
            {
                num = int.Parse(Console.ReadLine());
                digits=Utils.Digits(num, ref evens, ref ods);
                Console.WriteLine(Msg2,digits);
                Console.WriteLine(Msg3,evens);
                Console.WriteLine(Msg4,ods);
            }
            catch (Exception)
            {
                Console.WriteLine(Error);
            }
        }
    }
}
```
10. 
```c#
using System;
using LlibreriaSergi; //la llibreria es el projecte de C:\Users\isard\source\repos\LibreriaActivitatsC#SergiAlbalat
namespace ActivitatsProgramacio
{
    //Precon: L'usuari introdueix un any
    //Postcon: L'usuari sap si es un añy de traspass
    public class Activitats
    {
        public static void Main()
        {
            const string Msg1 = "Write a year and i will tell you if it's a leap year";
            const string Msg2 = "It is!";
            const string Msg3 = "It's not =(";
            const string Error = "The format of the number is incorrect";
            int year;
            Console.WriteLine(Msg1);
            try
            {
                year = int.Parse(Console.ReadLine());
                Console.WriteLine(Utils.Bisiesto(year)?Msg2:Msg3);
            }
            catch (Exception)
            {
                Console.WriteLine(Error);
            }
        }
    }
}
```
17. 
```c#
using System;
using LlibreriaSergi; //la llibreria es el projecte de C:\Users\isard\source\repos\LibreriaActivitatsC#SergiAlbalat
namespace ActivitatsProgramacio
{
    //Precon: L'usuari dos valors.
    //Postcon: L'usuari rep els valors intercanviats
    public class Activitats
    {
        public static void Main()
        {
            const string Msg1 = "How many numbers do you want to save?";
            const string Msg2 = "Your numbers:";
            const string Error = "The format of the number is incorrect";
            int max;
            Console.WriteLine(Msg1);
            try
            {
                max=int.Parse(Console.ReadLine());
                int[] numbers = new int[max];
                Utils.LlenarArray(ref numbers);
                Console.WriteLine(Msg2);
                Utils.EscribirArrays(ref numbers);
            }
            catch (Exception)
            {
                Console.WriteLine(Error);
            }
        }
    }
}
```