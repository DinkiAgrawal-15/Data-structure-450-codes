```java

public class largest_contigeous_subarray {
	// Java program to print largest contiguous array sum

	
		public static void main (String[] args)
		{
			int [] a = {-2, -3, 4, -1, -2, 1, 5, -3};
			System.out.println("Maximum contiguous sum is " +
										maxSubArraySum(a));
		}

		static int maxSubArraySum(int a[])
		{
			int size = a.length;
			int temp = Integer.MIN_VALUE, max_end = 0;

			for (int i = 0; i < size; i++)
			{
				max_end = max_end + a[i];
				if (temp < max_end)
					temp = max_end;
				if (max_end < 0)
					max_end = 0;
			}
			return temp;
		}
	}


```
