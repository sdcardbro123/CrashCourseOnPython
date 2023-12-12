## PYHON CODING QUESTIONS

Write a Python function to find the factorial of a number.

Write a Python function to check if a given number is prime.

Write a Python function to check if a given string is a palindrome.

Write a Python function to sort a list of numbers in ascending order.

Write a Python function to sort a list of strings in alphabetical order.

Write a Python function to count the number of occurrences of a character in a given string.

Write a Python function to find the second largest number in a list of numbers.

Write a Python function to find the second smallest number in a list of numbers.

Write a Python function to remove duplicate elements from a list.

Write a Python function to find the sum of all even numbers in a list.

Write a Python function to find the sum of all odd numbers in a list.

Write a Python function to find the sum of all numbers in a list.

Write a Python function to remove all even numbers from a list.

Write a Python function to remove all odd numbers from a list.

Write a Python function to merge two sorted lists into a single sorted list.

Write a Python function to find the maximum sum of any contiguous subarray of a list of numbers.

Write a Python function to find the length of the longest common subsequence of two given strings.

Write a Python function to find the greatest common divisor (GCD) of two numbers.

Write a Python function to find the least common multiple (LCM) of two numbers.

Write a Python function to convert a binary number to a decimal number.

Write a Python function to convert a decimal number to a binary number.

Write a Python function to convert a decimal number to a hexadecimal number.

Write a Python function to convert a hexadecimal number to a decimal number.

Write a Python function to convert a binary number to a hexadecimal number.

Write a Python function to convert a hexadecimal number to a binary number.

Write a Python function to find the first non-repeating character in a given string.

Write a Python function to find the missing number in a list of consecutive integers.

Write a Python function to check if two given strings are anagrams.

Write a Python function to find the maximum product of any three numbers in a list of numbers.

Write a Python function to find the maximum difference between any two elements in a list of numbers.

Write a Python function to find the maximum sum of any non-adjacent elements in a list of numbers.

Write a Python function to find the number of trailing zeros in the factorial of a given number.

Write a Python function to find the number of occurrences of each element in a given list.

Write a Python function to find the length of the longest palindrome in a given string.

Write a Python function to find the maximum sum of any contiguous subarray of a list of numbers, with the restriction that no two elements in the subarray are adjacent to each other.

Write a Python function to find the minimum number of coins required to make a given amount of change.

Write a Python function to find the number of ways to climb a staircase with n steps, given that you can only take one or two steps at a time.

Write a Python function to find the number of ways to partition a given set into k subsets.

Write a Python function to find the length of the longest increasing subsequence of a list of numbers.

Write a Python function to find the length of the longest

## The Python functions for the remaining clear questions:

```python
# 1
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n-1)

# 2
def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

# 3
def is_palindrome(s):
    return s == s[::-1]

# 4
def sort_numbers_ascending(lst):
    return sorted(lst)

# 5
def sort_strings_alphabetical(lst):
    return sorted(lst)

# 6
def count_char_occurrences(s, char):
    return s.count(char)

# 7
def second_largest_number(lst):
    return sorted(set(lst), reverse=True)[1]

# 8
def second_smallest_number(lst):
    return sorted(set(lst))[1]

# 9
def remove_duplicates(lst):
    return list(set(lst))

# 10
def sum_of_even_numbers(lst):
    return sum(num for num in lst if num % 2 == 0)

# 11
def sum_of_odd_numbers(lst):
    return sum(num for num in lst if num % 2 != 0)

# 12
def sum_of_numbers(lst):
    return sum(lst)

# 13
def remove_even_numbers(lst):
    return [num for num in lst if num % 2 != 0]

# 14
def remove_odd_numbers(lst):
    return [num for num in lst if num % 2 == 0]

# 15
def merge_sorted_lists(lst1, lst2):
    return sorted(lst1 + lst2)

# 16
def max_contiguous_subarray_sum(lst):
    max_sum = current_sum = lst[0]
    for num in lst[1:]:
        current_sum = max(num, current_sum + num)
        max_sum = max(max_sum, current_sum)
    return max_sum

# 18
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

# 19
def lcm(a, b):
    return abs(a * b) // gcd(a, b)

# 20
def binary_to_decimal(binary_str):
    return int(binary_str, 2)

# 21
def decimal_to_binary(decimal_num):
    return bin(decimal_num)[2:]

# 22
def decimal_to_hexadecimal(decimal_num):
    return hex(decimal_num)[2:]

# 23
def hexadecimal_to_decimal(hexadecimal_str):
    return int(hexadecimal_str, 16)

# 24
def binary_to_hexadecimal(binary_str):
    decimal_num = binary_to_decimal(binary_str)
    return decimal_to_hexadecimal(decimal_num)

# 25
def hexadecimal_to_binary(hexadecimal_str):
    decimal_num = hexadecimal_to_decimal(hexadecimal_str)
    return decimal_to_binary(decimal_num)

# 27
def missing_number(lst):
    n = len(lst) + 1
    expected_sum = n * (n + 1) // 2
    actual_sum = sum(lst)
    return expected_sum - actual_sum

# 28
def are_anagrams(str1, str2):
    return sorted(str1) == sorted(str2)

# 29
def max_product_of_three(lst):
    sorted_lst = sorted(lst)
    return max(sorted_lst[0] * sorted_lst[1] * sorted_lst[-1], sorted_lst[-3] * sorted_lst[-2] * sorted_lst[-1])

# 30
def max_difference_between_elements(lst):
    return max(lst) - min(lst)

# 31
def max_non_adjacent_subarray_sum(lst):
    incl = 0
    excl = 0
    for num in lst:
        new_excl = max(incl, excl)
        incl = excl + num
        excl = new_excl
    return max(incl, excl)

# 32
def trailing_zeros_factorial(n):
    count = 0
    i = 5
    while n // i > 0:
        count += n // i
        i *= 5
    return count

# 33
def occurrences_of_each_element(lst):
    from collections import Counter
    return Counter(lst)

# 35
def max_contiguous_subarray_sum_non_adjacent(lst):
    incl = 0
    excl = 0
    for num in lst:
        new_excl = max(incl, excl)
        incl = excl + num
        excl = new_excl
    return max(incl, excl)

# 37
def ways_to_climb_stairs(n):
    if n <= 1:
        return 1
    a, b = 1, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    return b
```
