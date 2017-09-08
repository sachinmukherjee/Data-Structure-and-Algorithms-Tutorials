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


#### Radix Sort
