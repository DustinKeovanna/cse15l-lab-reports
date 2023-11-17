# Lab Report #3

## Part 1 bugs
A test case where it's expected to fail and show the buggyness of the code.
```
public class ArrayExamples {
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
}
```
This is the Junit test 
```
@Test
  public void testingReversed() {
    int[] input1 = {2,5,4};
    int[] input2 = {4,5,2};
    assertArrayEquals(new int[]{4,5,2}, ArrayExamples.reversed(input1));
  }
```
A test case where it's expected to not fail and pass of the code.                                                                     
```
public class ArrayExamples {
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
}
```
This is the Junit test 
```
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
