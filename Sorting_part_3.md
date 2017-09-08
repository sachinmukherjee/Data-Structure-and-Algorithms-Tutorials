# Sorting 3

* Counting Sort
* Radix Sort
* Bucket Sort
* Heap Sort


### Counting Sort

It is not a comparision sort algorithm and gives O(n) complexity for sorting. It is used to place element direct into into place. It is usefull when range of input data is not significantly greater than the number of objects to be stored.

How it works

* Given an input array
* find the maximum and minimum from the input array
* Create an array from index minimum to maximum. Akk
* And fill than array Akk with the count of each number how many times occurs. for example if 11 occurs 2 times then fill the index 11 of array 2.
* Create a sum array Srr and fill it with the sum of previous index and current index to its current position. for example if index 3 count is 2 and index 4 count is 2 so the sum count of index 4 will be sum of index 3 and 4 i.e 4.
* Take an array Frr with number of element in the input and fill it with the index as sum count of element. for example 7 has a sum count of 3 in Srr so the Frr index 3 will contain element 7.
. We got the sorted array


### Radix Sort

It is same as Counting sort and Bucket Sort. It assumes that all numbers are from the same base b.

How it works

We are considering ascending order

* Since all the number are from 0 to 9 so we will be require 10 buckets.
* Find the largest number with number of digits it has and according to that fill all the digits with leading zeros so that all number will have same number of digits.
* Number of sorting pass required will be equal to number of digits in largest number
* Now sort the number from the first digit from right side. for example if a number is 010 to 0 is the right most digit. so place that number in index equal to right most digit value.
* Note that one index can contain many numbers so dont worry.
* Take numbers from bottom
* Again sort using 2nd digit from right side.
* Take number from bottom
* Again sort number using the 3rd digit from right side
* Repeat the process untill number of passes full fills it
* At last remove leading zeros




### Bucket Sort
