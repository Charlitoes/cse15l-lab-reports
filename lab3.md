Part 1: Bugs

A failure-inducing input for the buggy `ArrayTests.java` program would be if we were to put more than 1 number in the array
in the `testReverseInPlace` function. 

Example of the function:
`	public void testReverseInPlace() {`
`    int[] input1 = { 3 , 4, 5};`
`    ArrayExamples.reverseInPlace(input1);`
`    assertArrayEquals(new int[]{ 5, 4, 3 }, input1);`
`	}`

This would give us a test failure since the `reverseInPlace` method isn't actually reversing the array. 



An input that wouldn't produce a failure in the `ArrayTests.java` program would be if we were to put no elements or 1 element
in the array 

Example of the function: 
`	public void testReverseInPlace() {
    int[] input1 = { };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ }, input1);
	}`

The reason for this is that since there is nothing to be reversed or if there were only 1 element there wouldn't be any
change within the array itself and it would stay the same. 

Screenshots of the tests failing and passing with different values in the arrays:

![image](lab3_test-pass.png)

![image](lab3_test-fail.png)

The bug fixes before and after:

BEFORE:
`  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }`

AFTER: 
`  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }`

I made this change so when we try to reverse the array the first half of the numbers don't get immediately overwritten when we are trying to reverse the array, another notable change I made was that I made the for loop run for half of the time since the changes I made
allows the array to change 2 numbers per iteration instead of 1 number per iteration. 
