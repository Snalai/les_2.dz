﻿# les_2.dz
 package org.example.lesson2.HomeWork;

import java.util.Scanner;

public class HomeWork1 {
    public static void main(String[] args) {
        System.out.println("Сколько желаете ввести чисел?");
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        System.out.println("Вводите числа: ");
        System.out.println("Сумма простых чисел равна: " + domzadanie1(scanner, n));
    }

    /**
     * @apiNote Дана последовательность N целых чисел. Найти сумму простых чисел.
     * @param scanner вспомогательный класс
     * @param n длинна последовательности
     * @return сумма простых чисел sum
     */
    private static int domzadanie1(Scanner scanner, int n) {
        int sum = 0;
        for (int i = 0; i < n; i++) {
            int a = scanner.nextInt();
            if (a % 2 == 1) sum += a;
        }
        return sum;
    }
}

# les_2.dz
import java.util.Scanner;

public class HomeWork2 {
    public static void main(String[] args) {
        System.out.println("Сколько желаете ввести чисел?");
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        System.out.println("Вводите числа: ");
        System.out.println(domzadanie2(scanner, n));
    }
    /**
     * @apiNote Дана последовательность из N целых чисел. Верно ли, что последовательность является возрастающей.
     * @param scanner вспомогательный класс
     * @param n длинна последовательности
     * @return определение является ли последовательность возрастающей true/false
     */
    private static boolean domzadanie2(Scanner scanner, int n) {
        int a = 0;
        boolean c = true;
        for (int i = 0; i < n; i++) {
            int b = scanner.nextInt();
            if (b < a) {
                c = false;
            }
            a = b;
        }
        return c;
    }
}
# les_2.dz
package org.example.lesson2.HomeWork;

import java.util.Scanner;

public class HomeWork3 {
    public static void main(String[] args) {
        System.out.println("Сколько желаете ввести чисел?");
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] array = new int[n];
        int s = 0;
        for (int i = 0; i < array.length; i++) {
            array[i] = scanner.nextInt();
        }
        for (int p : domzadanie3(array, s)) {
            System.out.print(p + ", ");
        }
    }

    /**
     * @param array заполняемый нами массив чисел
     * @param s     счётчик для прохода по массиву
     * @return возвращает заменённые отрицательные числа в массиве на сумму индексов двузначных элементов массива
     * @apiNote Дан массив целых чисел. Заменить отрицательные элементы на сумму индексов двузначных элементов массива.
     */

    private static int[] domzadanie3(int[] array, int s) {
        int sum = 0;
        s = 0;
        for (int i : array) {

            if (i > 9) {
                sum += s;
            }
            s++;
        }
        s = 0;
        for (int j : array) {
            if (j < 0) {
                array[s] = sum;
            }
            s++;
        }
        return array;
    }
}

