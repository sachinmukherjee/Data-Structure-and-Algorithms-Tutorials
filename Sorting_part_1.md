# Sorting

## Topics Covered
 * Bubble Sort
 * Selection Sort
 * Insertion Sort

#### Introduction
Sorting is an algorithms which arrange elements in particular order either ascending or descending order.

#### Why Sorting
Some time sorting is important because it reduces the time complexity of the problem. We can use <i>sorting</i>  to reduce the time complexity of <i>search</i>.

<i>Best Case</i> : <b>O(nlogn)</b><br>
<i>Worst Case</i>: <b>O(n*n)</b>


### Bubble Sort
It is one of the simplest sorting algorithms. It works by iteration from the first element to the last element and then comparing each element and if necessary do swapping. It continues untill no swapping required. It get its name bubble because it bubbles the element to the top.

Considering Ascending order

![image](https://www.programiz.com/sites/tutorial2program/files/Bubble-sort-algorithm-programming.jpg)

Code for the Bubble sort considering ascending order

    void bubbleSort(int arr)
    {
      int len = arr.length;
      // for number of iteration to be made
      for(int i=0; i<n; i++)
      {
        // iterating through each element
        for(int j=0; j<n-1; j++)
        {
          if(arr[i]>arr[j])
          {
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
          }
        }
      }

    }

Here in first loop it number of iteration to be made and it is equal to number of elements and in second loop in iterates through each element and check the condition and make swapping according to the result of the condition.<br>
<i>Time Complexity</i> : <b>O(n*n)</b>

### Selection Sort

It is an in-place sorting algorithm. It works well for small files

    void selectionSort(int arr)
    {
      int len = arr.length;
      int min;
      for(int i=0; i<n-1; i++)
      {
        // considering min as first element of loop
        min  = i;
        // iterating for one step ahead of value of i
        for(int j = i+1; j<n; j++)
        {
          if(arr[i]> arr[j])
          // if condition becomes true then assigning index of j as min
          min  = j;
        }
        // now swapping elements
        int temp = arr[min];
        arr[min] = arr[i];
        arr[i] = temp;
      }

    }

It selects an element and compare it with other element in increasing index order and make swapping according to that.<br>
<i>Time Complexity</i> : <b>O(n*n)</b><br>


### Insertion Sort

It removes an element from input data and insert it into correct position. It is efficient for small data and more efficient that bubble and selection sort.

    void insertionSort(int arr)
    {
      int len = arr.length;
      // pick an index greater than 0
      for(int i=1; i<len; i++)
      {
        // move backwards from that index
        for(int j=i; j>0; j--)
        {
          // condition
          if(arr[j]<arr[j-1])
          {
            // swapping
            int temp = arr[j];
            arr[j] = arr[j-1];
            arr[j-1] = temp;
          }
        }
      }
    }

It picks an index and then move backwards and compare element according to that and make necessary swapping.<br>
<i>Time Complexity</i>: <b>O(n*n)</b> <br>
