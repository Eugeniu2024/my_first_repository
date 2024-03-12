Задача 1: Задайте значения M и N. Напишите программу, которая выведет все натуральные числа в промежутке от M до N.
 Использовать рекурсию, не использовать

using System;

class Program
{
    static void Main()
    {
        int m = 3;
        int n = 8;

        PrintNaturalNumbersInRange(m, n);
    }

    static void PrintNaturalNumbersInRange(int m, int n)
    {
        if (m <= n)
        {
            Console.WriteLine(m);
            PrintNaturalNumbersInRange(m + 1, n);
        }
    }
}





Задача 2: Напишите программу вычисления функции Аккермана с помощью рекурсии.
 Даны два неотрицательных числа m и n.

class Program
{
    static void Main()
    {
        int m = 2;
        int n = 1;

        Console.WriteLine($"A({m}, {n}) = {Ackermann(m, n)}");
    }

    static int Ackermann(int m, int n)
    {
        if (m == 0)
        {
            return n + 1;
        }
        else if (n == 0)
        {
            return Ackermann(m - 1, 1);
        }
        else
        {
            return Ackermann(m - 1, Ackermann(m, n - 1));
        }
    }
}






Задача 3: Задайте произвольный массив. Выведете его элементы, начиная с конца.
 Использовать рекурсию, не использовать циклы.


 using System;

class Program
{
    static void Main()
    {
        int[] array = { 13,19,21,33,91};
        PrintArrayReversed(array, array.Length - 1);
    }

    static void PrintArrayReversed(int[] array, int index)
    {
        if (index < 0)
            return;

        Console.WriteLine(array[index]);
        PrintArrayReversed(array, index - 1);
    }
}
