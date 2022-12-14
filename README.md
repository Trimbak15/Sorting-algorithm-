# Sorting-algorithm-
Study related the sorting algorithms to sort the elements....



import java.util.*;
import java.lang.*;
import java.io.*;

public class Main
{
	public static void main (String[] args) throws java.lang.Exception
	{
		//your code here
		// bubble sort - in this sorting algorithm we used to sort the element by their adjacent side of there element
		// i.e (ascending order) -- 1 4 2 3 6 --- 1 2 3 4 6 ***it will directly sort the element in ascending order***
		// i.e (decending order) -- 1 4 2 3 6 --- 4 2 3 6 1 -- 4 3 6 2 1 -- 4 6 3 2 1 -- 6 4 3 2 1
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int arr[] = new int[n];

		for(int i=0;i<n;i++)
			{
				arr[i] = sc.nextInt();
			}
		// for(int i=0;i<(n-1);i++)
		// 	{
		// 		for(int j=0;j<(n-1-i);j++)
		// 			{
		// 				// ascending order
		// 				// if(arr[j] > arr[j+1])
		// 				// {
		// 				// 	int temp = arr[j];
		// 				// 	arr[j] = arr[j+1];
		// 				// 	arr[j+1] = temp;
		// 				// }

		// 				// decending order
		// 				if(arr[j] < arr[j+1])
		// 				{
		// 					int temp = arr[j];
		// 					arr[j] = arr[j+1];
		// 					arr[j+1] = temp;
		// 				}
		// 			}
		// 		for(int k=0;k<n;k++)
		// 	{
		// 		System.out.print(arr[k]+" ");
		// 	}
		// 		System.out.println();
		// 	}
		// // for(int i=0;i<n;i++)
		// // 	{
		// // 		System.out.print(arr[i]+" ");
		// // 	}


		// selection sort - in this ype of soring algorithm we used to see the swapping between the ith element ---- firstly we find the minimal element of it and then its index so that the element should iterate one by one
		// i.e (ascending order) --- 1 4 2 3 6 -- 1 2 4 3 6 -- 1 2 3 4 6
		// i.e (decending order) --- 1 4 2 3 6 -- 6 4 2 3 1 -- 6 4 3 2 1

		// for(int i=0;i<(n-1);i++)
		// 	{
		// 		int minimumElement = arr[i];
		// 		int indexOfMin = i;
		// 		for(int j=i+1;j<n;j++)
		// 			{
		// 				//ascending order
		// 				// if(arr[j] < minimumElement)
		// 				// {
		// 				// 	minimumElement = arr[j];
		// 				// 	indexOfMin = j;
		// 				// }

		// 				//descending order
		// 				if(arr[j] > minimumElement)
		// 				{
		// 					minimumElement = arr[j];
		// 					indexOfMin = j;
		// 				}
		// 			}
		// 		int temp = arr[i];
		// 		arr[i] = arr[indexOfMin];
		// 		arr[indexOfMin] = temp;
		// 		for(int k=0;k<n;k++)
		// 	{
		// 		System.out.print(arr[k]+" ");
		// 	}
		// 		System.out.println();
		// 	}
		// for(int k=0;k<n;k++)
		// 	{
		// 		System.out.print(arr[k]+" ");
		// 	}


		// insertion sort - in this sorting algorithm we used to swap the element only after selecting some specific element 
		// i.e --- 1 2 3 6 5 -- 1 2 3 5 6 
		// in above example the first threee element is sorted mode remaining element we have to slect and check its correct position

		for(int i=0;i<(n);i++) // forward direction loop is running
			{
				int element = arr[i];
				int j = i-1;
				while(j>=0 && arr[j] > element) // backward direction loop is running
					{
						arr[j+1] = arr[j];
						j = j-1;
					}
				arr[j+1] = element;
			}
		for(int k=0;k<n;k++)
					{
						System.out.print(arr[k]+" ");
					}		
	}
}

