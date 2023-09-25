# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->

# Approach
<!-- Describe your approach to solving the problem. -->
- Create a map mp, to store key-value pair, i.e. element-frequency pair.
- Traverse the array from start to end.
- For every element in the array update mp[array[i]]++
- Store the element-frequency pair in a vector and sort the vector in decreasing order of frequency.
- Print the first k elements of the sorted array.
# Complexity
- Time complexity:
<!-- Add your time complexity here, e.g. $$O(n)$$ -->
O(D log D), where D is the count of distinct elements in the array

- Space complexity:
<!-- Add your space complexity here, e.g. $$O(n)$$ -->
O(D log D), where D is the count of distinct elements in the array

# Code
```
class Solution {

    public static ArrayList sort_by_value(ArrayList al) {

		Collections.sort(al, new Comparator<Map.Entry<Integer, Integer>>() {
			@Override
			public int compare(Map.Entry<Integer, Integer> o1, Map.Entry<Integer, Integer> o2){
				  if (o1.getValue() == o2.getValue())
                        return o2.getKey() - o1.getKey();
                    else
                        return o2.getValue()
                            - o1.getValue();
			}
		});
		return al;
	}

    public int[] topKFrequent(int[] nums, int k) {
        
        int l= nums.length;
        HashMap<Integer, Integer> mp = new HashMap<>();

    
        for(int i=0;i<l;i++)
        {
            mp.put(nums[i], mp.getOrDefault(nums[i], 0) + 1);
        }

        List<Map.Entry<Integer, Integer> > list = new ArrayList<Map.Entry<Integer, Integer> >(mp.entrySet());

        Collections.sort(
            list,
            new Comparator<Map.Entry<Integer, Integer> >() {
                public int compare(
                    Map.Entry<Integer, Integer> o1,
                    Map.Entry<Integer, Integer> o2)
                {
                    if (o1.getValue() == o2.getValue())
                        return o2.getKey() - o1.getKey();
                    else
                        return o2.getValue()
                            - o1.getValue();
                }
            });
        
        int answer[]= new int[k];
        int count =0;

         for (int i = 0; i < k; i++)
            answer[count++]=list.get(i).getKey();
        return(answer);
    }
}
```
