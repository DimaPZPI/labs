using System;

public class MatrixPrinter
{
    public static void PrintMatrixByType<T>(T[,] matrix, Type targetType)
    {
        // Перевіряємо, чи матриця не є null
        if (matrix == null)
        {
            Console.WriteLine("Матриця є null.");
            return;
        }

        // Отримуємо розміри матриці
        int rows = matrix.GetLength(0);
        int cols = matrix.GetLength(1);

        Console.WriteLine($"Матриця (розміром {rows}x{cols}) з елементами типу: {targetType.Name}");

        // Проходимо по кожному елементу матриці
        for (int i = 0; i < rows; i++)
        {
            for (int j = 0; j < cols; j++)
            {
                // Перевіряємо, чи тип поточного елемента відповідає вказаному типу
                if (matrix[i, j] != null && matrix[i, j].GetType() == targetType)
                {
                    // Виводимо елемент, якщо його тип збігається
                    Console.Write(matrix[i, j] + "\t");
                }
                else
                {
                    // Якщо тип не збігається, виводимо пробіл або інший символ, щоб зберегти структуру матриці
                    Console.Write(" \t"); // Можна змінити на інший символ, наприклад ".\t"
                }
            }
            Console.WriteLine(); // Переходимо на новий рядок після кожного рядка матриці
        }
    }

    public static void Main(string[] args)
    {
        // Приклад використання:

        // Створюємо матрицю, що містить різні типи даних
        object[,] mixedMatrix = {
            { 1, "hello", 3.14 },
            { true, 5, 'a' },
            { 10.5f, null, 7 }
        };

        Console.WriteLine("Вихід для цілих чисел (int):");
        PrintMatrixByType(mixedMatrix, typeof(int));
        Console.WriteLine();

        Console.WriteLine("Вихід для рядків (string):");
        PrintMatrixByType(mixedMatrix, typeof(string));
        Console.WriteLine();

        Console.WriteLine("Вихід для дійсних чисел (double):");
        PrintMatrixByType(mixedMatrix, typeof(double));
        Console.WriteLine();

        Console.WriteLine("Вихід для булевих значень (bool):");
        PrintMatrixByType(mixedMatrix, typeof(bool));
        Console.WriteLine();

        Console.WriteLine("Вихід для символів (char):");
        PrintMatrixByType(mixedMatrix, typeof(char));
        Console.WriteLine();
    }
}
