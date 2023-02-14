import java.util.HashMap;
public class Solution {

	public static int getPairsWithDifferenceK(int arr[], int k) {
		//Write your code here
        
        HashMap<Integer, Integer> map = new HashMap<>();
		int pairCount = 0;
		for(int item:arr) 
		{
			int p1 = item + k;
			boolean flag = false;
			if(item == p1) 
			{
				flag = true; //this case is there for k=0
			}
			if(map.containsKey(p1)) 
			{
			  pairCount += map.get(p1);	
			}
			int p2 = item - k;
			if(map.containsKey(p2) && !flag)
			{
				pairCount += map.get(p2);
			}
			if(map.containsKey(item)) {
				map.put(item, map.get(item)+1);
			}else {
				map.put(item, 1);
			}
		}
		return pairCount;
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int arr[] = {5,1,2,4};
		int arr1[] = {4,4,4,4};
		System.out.println(getPairsWithDifferenceK(arr, 3));  //2
		System.out.println(getPairsWithDifferenceK(arr1, 0)); //6
	}
}
