# Sorting

 * Merge Sort
 * Shell Sort
 * Quick Sort
 * Tree Sort


### Merge Sort

Mergining is the process of combining two sorted files to make a bigger file. Selection is the process of dividing a large file into two parts k small elements and n-k large elements. It is used for sorting linked list.

We have to first divide the file and sort them and then merge them.<br>

    void merge(int arr[], int left, int right, int mid)
    {
      int k = 0;  // for new array index
      int n1 = right - left +1 ;  // for left array
      int n2 = right - mid;       // for right array
      int L[] = new int[n1];      // creating two new arrays
      int R[] = new int[n2];

      // comping divided array into two new arrays left and right
      for(i=0; i<n1; i++)
      {
        L[i] = arr[i+left];
      }

      for(j=0; j<n2; j++)
      {
        R[j] = arr[mid+1+j];
      }
      // loop continues untill i and j is smaller than number of array elements
      while(i<n1 && j<n2)
      {
        // if element of left array is smaller than right array then copy the element of left array
        if(L[i]<R[i])
        {
          arr[k] = L[i];
          i++;
          k++
        }
        // else copy the element of right array
        else
        {
          arr[k] = R[j];
          k++;
          j++;
        }
      }
      // copying remaining elements
      while(i<n1)
      {
        arr[k] = L[i];
        i++;
        k++;
      }
      while(j<n2)
      {
        arr[k] = R[j];
        j++;
        k++;
      }
    }
    // Function for sorting
    void sort(int arr[], int l, int r)
    {
      if(l<r)
       {
        int m = (r+l)/2;
        sort(arr, l, m);
        sort(arr,m+1, r);
        arr(arr, l, r, m);
       }
    }
<i> Time Complexity</i> : <b> O(n*logn)</b>

### Quick Sort

It is example of divide and conquire algorithm and It is also called partition exchange sort. It consist of four steps.<br>

Algorithm
* If there are one or more elements in the arrays to be sorted return
* Pick an element in the array to serve as 'pivot' point. Take pivot as last element.
* Split the array into two parts one with element larger then the pivot and other smaller than the pivot
* Recursively repeat the algorithm for both half of original array


    int partition(int arr[], int low, int high)
    {
      int pivot = arr[high];
      int i = low-1;
      for(int j=low; j<high-1; j++)
      {
        if(arr[j]<=pivot)
        {
          i++;
          int temp = arr[i];
          arr[i] = arr[j];
          arr[j] = temp;
        }
      }
      int temp = arr[i+1];
      arr[i+1] = arr[high];
      arr[high] = temp;

      return i+1;
     }


    void sort(int arr[], int low, int high)
    {
      if(low<high)
      {
        int mid = partition(arr, low, high);
        sort(arr, low, mid);
        sort(arr, mid+1, high);
      }
    }
<i> Time Complexity<i> : <b> O(n*logn)</b>

Illustration of Partion

    arr[] : {10, 80, 30, 90, 40, 50, 70}
    low = 0, high = 6, pivot = arr[h] = 70
    Initialize index of smaller element, i = -1

    Transverse element from j = low to high-1
    j=0 since arr[]
