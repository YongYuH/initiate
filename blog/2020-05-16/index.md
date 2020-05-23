---
date: "2020-05-16"
title: "Rearrange an array so that arr[i] becomes arr[arr[i]]"
category: "Algorithm"
tags: ['algorithm',  'brute-force', 'geeksforgeeks', 'java']
banner: "/initiate/assets/bg/1.jpg"
---
# Rearrange an array so that arr[i] becomes arr[arr[i]]

[question link](https://www.geeksforgeeks.org/rearrange-given-array-place/)

solution:  
```java
class Rearrange {
  static int[] rearrangeListWithLongExtraSpace(int[] input) {
    int arrayLength = input.length;
    int result[] = new int[arrayLength];
    
    for (int i = 0; i < arrayLength; i++) {
      int originalValue = input[i];
      int updatedValue = input[originalValue];
      result[i] = updatedValue;
    }
    
    return result;
  }

  public static void main(String[] args) {
    int[] input = new int[]{3, 2, 0, 1};
    int[] output = rearrangeListWithLongExtraSpace(input);
    System.out.println(Arrays.toString(output));
  }
}
```

Space Complexity: O(n)
