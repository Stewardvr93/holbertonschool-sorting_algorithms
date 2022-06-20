
# 0x1B. C - Sorting algorithms & Big O

![](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-low_level_programming/248/willy-wonka.png)

------------

## General

-At least four different sorting algorithms
-What is the Big O notation, and how to evaluate the time complexity of an algorithm
-How to select the best sorting algorithm for a given input
-What is a stable sorting algorithm

------------

# More Info

## Data Structure and Functions

 -For this project you are given the following print_array, and print_list functions:

```
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
```
```
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}
```
```
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
```
------------

## Big-O Notation

Asymptotic notation is a set of languages which allow us to express the performance of our algorithms in relation to their input. Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.


![](https://raw.githubusercontent.com/developerinsider/developer-insider-content/master/POST/C/Tuto/BigO/BigOComplexity.png)

## Main orders of complexity

|  Order | Name |
| ------------ | ------------ |
| O(1)  | constante |
| O(log n) | logarítmica |
| O(n) | lineal |
| O(n log n) | casi lineal |
| O(n^²) | cuadrática |
| O(n^³) | cúbica |
| O(2^n) | exponencial |

## Examples:

# O(1)
```
void f(int n)
{
    printf("n = %d\n", n);
}
```
This function runs in O(1) time (or "constant time") relative to its input. The input array could be 1 item or 1,000 items, but this function would still just require one step.

# O(n)
```
void f(int n)
{
    int i;

    for (i = 0; i < n; i++)
    {
        printf("[%d]\n", i);
    }
}
```
This function runs in O(n) time (or "linear time"), where n is the number of items in the array. If the array has 10 items, we have to print 10 times. If it has 1000 items, we have to print 1000 times.

# O(n^2)
```
void f(int n)
{
    int i;
    int j;

    for (i = 0; i < n; i++)
    {
        if (i % 2 == 0)
        {
            for (j = 1; j < n; j = j * 2)
            {
                printf("[%d] [%d]\n", i, j);
            }
        }
        else
        {
            for (j = 0; j < n; j = j + 2)
            {
                printf("[%d] [%d]\n", i, j);
            }
        }
    }
}
```

------------



| Task | Task description |
| ------------ | ------------ |
| Task 0 | Bubble sort |
| Task 1 | Insertion sort |
| Task 2 | Selection sort |
| Task 3 | Quick sort |

------------


