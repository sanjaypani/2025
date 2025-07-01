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

5. Difference Between ExecutorSevrice & ThreadPool ?
6. explain CAP theorem ?
7. Explain Saga Pattern ?
8. advantage of consumer group in kafka ?
9. what is consumer offset ?
10. what ack status 0,1 and all in kafka ?
11. what is the formula you are using for creating partition and replication factor for your kafka broker in your project ?
12. what scenario you will go for kafka based aproach ?
13. when to use sql vs NoSql ?
14. Explain JWT Token and how you are going to implement it ?
15. what is http 403 how it will be generated ?
16. Spring Boot Performance improvement ?
17. 3 tier application running in AWS (Spring boot + Microservices + Any DB + Any UI framework). Users facing latency issue how you are gonna troubleshoot ?
18. same sceenario lets say url is not wokring how you aregonna trouble shoot ?
19. In our Porejct lets say Docker image is more (nearly 1 GB), how are you gonna reduce the size ?
20. Docker EntryPoint VS CMD VS Run ? explain with same example
  

5. Question 4 : lets Say array is unsorted how to apparoach using <2 pointer Technique> ?

Ans : 

	Solution 1: Sort the Array and then Follow Question 4 Answer : O(n*log(n)) : due to Sorting
	Solution 2 : Without using <2 pointer Technique> : Use HashSet O(n) 
