---
date: "2020-05-23"
title: "Maximum water that can be stored between two buildings"
category: "Algorithm"
tags: ['algorithm',  'brute-force', 'geeksforgeeks', 'java']
banner: "/initiate/assets/bg/1.jpg"
---
# Maximum water that can be stored between two buildings

[question link](https://www.geeksforgeeks.org/maximum-water-that-can-be-stored-between-two-buildings/)

solution:  
```java
class MaximumWater {
  static int getPairMax (int[] input) {
    int maxTrapped = 0;

    for (int i = 0; i < input.length; i++) {
      int heightOfstartIndex = input[i];

      for (int j = 0; j < input.length; j++) {
        int gapWidth = Math.abs(j - i - 1);
        int minHeight = Math.min(input[i], input[j]);       
        int trapped = (j - i) <= 1 ? 0 : gapWidth * minHeight;
        maxTrapped = Math.max(maxTrapped, trapped);
      }
    }

    return maxTrapped;
  }

  public static void main (String[] args) {
    int[] input = {1, 3, 4};
    int result = getPairMax(input);
    System.out.println("result");
    System.out.println(result);

    int[] input2 = {2, 1, 3, 4, 6, 5};
    int result2 = getPairMax(input2);
    System.out.println("result2");
    System.out.println(result2);
  }
}
```  

Time Complexity: O(n^2)

