Maximum scalar product of two vector
Here, in this page we will discuss the program to find maximum scalar product of two vector in java programming language. We are given with two arrays and need to return the maximum product that obtained.

Maximum scalar product of two vector in java
Here, we will discuss the two different ways for solving the problem. These two different ways are :

Method 1 : Sorting Without using inbuilt function.
Method 2 : Sorting using inbuilt sort function.
Method 1 :
Sort the first and second array in ascending order,
Declare a variable say product = 0.
Run a loop from index 0 to n
Set product += (arrr1[i]*arr2[i])
After complete iteration print product.
Time and Space Complexity :
Time Complexity : O(n2)
Space Complexity : O(1)
C++ program to find maximum scalar product of two vector
Related Pages
Removing Duplicate elements from an array

Finding Minimum scalar product of two vectors

Counting the number of even and odd elements in an array 

Find all Symmetric pairs in an array 

Find maximum product sub-array in a given array

Method 1 : Code in Java
Run
class Main
{
    public static void main (String[] args)
    {
           int arr1[] = {1, 2, 6, 3, 7};
           int arr2[] = {10, 7, 45, 3, 7};
           int n = arr1.length;

           //Sort arr1 in ascending order
           for(int i=0; i<n; i++){
                for(int j=i+1; j<n; j++){ if(arr1[i]>arr1[j]){
                       int temp = arr1[i];
                       arr1[i] = arr1[j];
                       arr1[j] = temp;
                    }
                }
            }

           //Sort arr2 in ascending order
           for(int i=0; i<n; i++){
                for(int j=i+1; j<n; j++){ if(arr2[i]>arr2[j]){
                        int temp = arr2[i];
                        arr2[i] = arr2[j];
                        arr2[j] = temp;
                    }
                 }
            }

          int product = 0;
          for(int i=0; i<n; i++)
              product += arr1[i]*arr2[i];

          System.out.print(product);
   }
}
Output
413
Method 2 :
In this method we will use inbuilt sort function to sort the array.

For, sorting arr1 in ascending order, use Arrays.sort(arr1)
For, sorting arr2 in descending order, use Arrays.sort(arr2, Collections.reverseOrder());.
Time and Space Complexity :
Time Complexity : O(n log(n))
Space Complexity : O(1)
Arrays.sort() in Java
An array class is a class containing static methods that are used with arrays in order to search, sort, compare, inserting elements, or returning a string representation of an array.
Arrays.sort() method consists of two variations one in which we do not pass any arguments where it sort down the complete array
Method 2 : Code in Java
Run
import java.util.Arrays;
import java.util.Collections;
class Main
{
    public static void main (String[] args)
    {
          Integer arr1[] = {1, 2, 6, 3, 7};
          Integer arr2[] = {10, 7, 45, 3, 7};
          int n = arr1.length;

          //Sort arr1 in ascending order
          Arrays.sort(arr1);

          //Sort arr2 in ascending order
          Arrays.sort(arr2);

          int product = 0;
          for(int i=0; i<n; i++)
              product += arr1[i]*arr2[i];

          System.out.print(product);
   }
}
Output
413
