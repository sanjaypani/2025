"# 2025" Preparation

1. Morgan Stanley : DeadLock Programm (Done)
2. find the secone largest element in array using stream API ?

Ans : 

	int [] arr = {45, 7, 90, 67, 12, 36, 77};
    int secondNumber = Arrays.stream(arr)
                                  .boxed()
                                  .skip(1)
                                  .findFirst()
                                  .orElse(0); // if not found then return 0

    System.out.println("secondNumber is " + secondNumber);
