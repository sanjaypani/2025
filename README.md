"# 2025" Preparation

1. DeadLock Programm : Use any of the sites to practice

2. find the second element in array using stream API ?

Ans : 

	int [] arr = {45, 7, 90, 67, 12, 36, 77};
    int secondNumber = Arrays.stream(arr)
                                  .boxed()
                                  .skip(1)
                                  .findFirst()
                                  .orElse(0); // if not found then return 0

    System.out.println("secondNumber is " + secondNumber);

3. Move all Zero's to End ? (Using Stream API)

Ans : 

	int [] arr = {1, 2, 0, 4, 3, 0, 5, 0};
	
	List<Integer> list = Arrays.stream(arr).boxed().toList();  // convert int [] to Integer List
    List<Integer> collect = Stream.concat(list.stream().filter(n -> n != 0), list.stream().filter(n -> n == 0)).collect(Collectors.toList());
    System.out.println(collect);
	
4. Two Sum Problem Using <2 pointer Technique> when array is sorted.

Ans :

	int [] arr = {2,3,4,5,6};
    int target = 10;
	
	private static int[] twoSum(int[] arr, int target) {
        int left = 0;
        int right = arr.length -1;

        while (left < right) {
            int currentSum = arr[left] + arr[right];
            if(currentSum == target) {
                return new int[] {left, right};
            }
            else if (currentSum < target) {
                left++;
            } else {
                right--;
            }
        }
        return null;
    }
	
Output : 2 & 4 <index>	

5. Question 4 : lets Say array is unsorted how to apparoach using <2 pointer Technique> ?

Ans : 

	Solution 1: Sort the Array and then Follow Question 4 Answer : O(n*log(n)) : due to Sorting
	Solution 2 : Without using <2 pointer Technique> : Use HashSet O(n) 