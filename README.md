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