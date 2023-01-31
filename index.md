## Lab Report 2: Part 1
I wrote a StringServer that was based off of Lab 2's NumberServer.java | 
Below is the code
![](https://i.imgur.com/9xOdrxi.png)
If we type in http://localhost:2000/add-message?s=Hello we get
![](https://i.imgur.com/82usQ2w.png)
Many methods are being called to achieve the screenshot:
1. `getPath().contains("/add-message")` which tells us that we are adding a String to the message
2. `getQuery().split("=")` which gives us an array with 2 indices coming from the URL splitting at =
3. `strings.add(parameters[1] + " ")` which adds a new string to the Strings arrayList
Now if we replace "Hello" with "This is This is Lab Report 2" we get:
![](https://i.imgur.com/r6hOuzY.png)
Many of the same methods as before are called to achieve that screenshot some more that are used are:
1) `strings.size()` which gets the size of the ArrayList
2) `strings.get(i)` which gets the element inside of the ArrayList to create the message
3) `String.format("%s\n", message)` which creates the message that will be stated in server
The values of this class changed to Strings from what the Lab 2 was, ints. The URL's value was split into Strings and put into an array in order to be printed and processed correctly.
## Lab Report 2: Part 2
- A faulty input that resulted in a failure output was
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = {1,2,3,4,5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 5,4,3,2,1 }, input1);
	}
```

![](https://i.imgur.com/2rp5v9m.png) What happens after it is run
This is faulty because the output ends up as 5,4,3,4,5
- An input that didn't create a faulty error in the code was 
```
@Test
	public void testReverseInPlace() {
    int[] input1 = { 5 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 5 }, input1);
	}
  ```
  ![](https://i.imgur.com/Ichxh1J.png) What happens after it is run
  This has the correct output because there is only one input so nothing to reverse
  
  To fix this the code was changed from
  ```
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  ```
  to
  ```
    int[] newArray = new int[arr.length];
    for (int j =0; j< arr.length; j++){
      newArray[j] = arr[j];
    }
    for (int i =0; i< arr.length; i++){
      arr[i] = newArray[arr.length-1-i]; 
    }
   ```
   We added a temporary deep copy of the past array and copied the reverse to our past array. 
This is necessary because previously the code would be re-written and half of the numbers would've disappeared.
## Lab Report 2: Part 3
Lab 2 has taught me how to create a server and how to use methods in the import 
```
import java.io.IOException;
import java.net.URI;
```
Furthermore, it has taught me how to use JUnit to debug correctly. Previously I only saw JUnit as a bother, however, now I see it as a tool to help correct my code.
