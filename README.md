# Arranging-max-Min-element-in-order
Taking an array as input and arrange the elements of array an alternative series of max and max
import java.util.Scanner;
import java.util.Arrays;
public class MaxMinElementsOfArr {
	public void  maxMinElementsOfArr(int arr[],int n) {
		//int n=arr.length;
		Arrays.sort(arr);
		int max_idx=n-1;
		int min_idx=0;
		int arr1[]=new int[n];
		for(int i=0;i<arr.length;i++) {
			if(i%2==0) {
				int temp=arr[max_idx];
				arr[max_idx]=arr1[i];
				arr1[i]=temp;
				max_idx--;
			}
			else
			{
				int temp=arr[min_idx];
				arr[min_idx]=arr1[i];
				arr1[i]=temp;
				min_idx++;
				
			}
		}
		for(int i:arr1)
		System.out.println(i);
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		System.out.println("enter array size: ");
		int n=sc.nextInt();
		System.out.println("enter array elements: ");
		int arr[]=new int[n];
		for(int i=0;i<n;i++) {
			arr[i]=sc.nextInt();
		}
		 MaxMinElementsOfArr obj=new  MaxMinElementsOfArr();
		 obj. maxMinElementsOfArr(arr,n);
		 sc.close();
		
			

	}

}
