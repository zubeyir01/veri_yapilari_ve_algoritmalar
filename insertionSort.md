# Insertion Sort 
```java
// Java program for implementation of Insertion Sort
class InsertionSort {
    /*Function to sort array using insertion sort*/
    void sort(int arr[])
    {
        int n = arr.length;
        for (int i = 1; i < n; ++i) {
            int key = arr[i];
            int j = i - 1;
 
            /* Move elements of arr[0..i-1], that are
               greater than key, to one position ahead
               of their current position */
            while (j >= 0 && arr[j] > key) {
                arr[j + 1] = arr[j];
                j = j - 1;
            }
            arr[j + 1] = key;
        }
    }
 
    /* A utility function to print array of size n*/
    static void printArray(int arr[])
    {
        int n = arr.length;
        for (int i = 0; i < n; ++i)
            System.out.print(arr[i] + " ");
 
        System.out.println();
    }
 
    // Driver method
    public static void main(String args[])
    {
        int arr[] = { 12, 11, 13, 5, 6 };
 
        InsertionSort ob = new InsertionSort();
        ob.sort(arr);
 
        printArray(arr);
    }
}
```
## Insertion Sort Steps
**[22,27,16,2,18,6]**

## A) **Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.** 

-   1.ADIMIN SONUNDA OLUŞAN DİZİNİN HALİ 

    [22,27,16,2,18,6]

-   2.ADIMIN SONUNDA OLUŞAN DİZİNİN HALİ

    [16,22,27,2,18,6]

-   3.ADIMIN SONUNDA OLUŞAN DİZİNİN HALİ
    
    [2,16,22,27,18,6]

-   4.ADIMIN SONUNDA OLUŞAN DİZİNİN HALİ  

    [2,16,18,22,27,6]

-   5.ADIMIN SONUNDA OLUŞAN DİZİNİN HALİ   

    [2,6,16,18,22,27]

***5 adımda dizi küçükten büyüğe sıralanmış oldu.***   

## B) Big-O gösterimini yazınız. 
    Worst case:
     O(n^2)

## C)  Time Complexity

    O(n^2)

## D) Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.

    Avarage Case


# [7,3,5,8,2,9,4,15,6] dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.  

-  [3,7,5,8,2,9,4,15,6]
-  [3,5,7,8,2,9,4,15,6]
-  [3,5,7,8,2,9,4,15,6] 
-  [2,3,5,7,8,9,4,15,6]