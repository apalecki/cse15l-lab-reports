# Part 1

## Failure-inducing
```
    @Test
    public void testReversed() {
        int[] inputArray = {1, 2, 3, 4, 5};
        int[] reversedArray = YourClass.reversed(inputArray);
        int[] expectedArray = {5, 4, 3, 2, 1};

        // This will fail because the reversedArray will not be as expected
        assertArrayEquals(expectedArray, reversedArray);
```
This input for the `reversed()` method will fail since there is a bug where the assignment was done to `arr[i]` instead of `newArray[i]`.


## Doesn't induce a failure
```
    @Test
    public void testReversedWithAlreadyReversedArray() {
        int[] inputArray = {5, 4, 3, 2, 1};
        int[] reversedArray = YourClass.reversed(inputArray);
        int[] expectedArray = {1, 2, 3, 4, 5};

        // This should pass because the original bug doesn't affect already reversed arrays
        assertArrayEquals(expectedArray, reversedArray);
```

This inp for the `reversed()` method shouldn't induce a failure because the `inputArray` is already sorted in reverse order.

## Fixing the bug
Before
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
After
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
This fixes the issue because now it uses the correct array assignment in the for loop and it also returns the correct array now.

# Part 2

## Researching grep command
1) `grep "pattern" filename`

input- `grep "pattern" chapter-1.txt`

output-  ```Radar data show the Otis fighters were airborne at 8:53. Lacking a target, they were vectored toward military-controlled airspace off the Long Island coast. To avoid New York area air traffic and uncertain about what to do, the fighters were brought down to military airspace to "hold as needed." From 9:09 to 9:13, the Otis fighters stayed in this holding pattern.```

input- `grep "pattern" chapter-2.txt`

output- `This pattern of expansion through building alliances extended to the United States. A`

2) `grep -A[NumberOfLines(n)] [search] [file]`

input- `grep -A1 radar chapter-1.txt`

output- ``` At 8:41, in American's operations center, a colleague told Marquis that the air traffic controllers declared Flight 11 a hijacking and "think he's [American 11] headed toward Kennedy [airport in New York City]. They're moving everybody out of the way. They seem to have him on a primary radar. They seem to think that he is descending."```

input- `grep -A1 red chapter-2.txt`

output- ```declared war against God and his messenger, they called for the murder of any
                American, anywhere on earth, as the "individual duty for every Muslim who can do it```

3) `grep -R [Search]`

input- `grep -R alarmed`

output- `government/Media/Domestic_Violence_Ruling.txt:Judge Thornton's ruling has alarmed advocates for battered
government/Media/Too_Crucial_to_Take_Cut.txt:admittedly are alarmed. How can we resuscitate an already sick`

input- `grep -R green`

output- ```911report/chapter-13.4.txt:                twice explored the possibility of obtaining a U.S. green card shortly before his
911report/chapter-5.txt:                at Atef 's urging, finally decided to give KSM the green light for the 9/11
911report/chapter-6.txt:                CIA had worried that giving him a green light might cross the line into violation of
biomed/1471-2091-3-22.txt:          expressed as fusion proteins with green fluorescent
biomed/1471-2105-3-14.txt:          http://ucjeps.berkeley.edu/bryolab/greenplantpage.html,
biomed/1471-2105-3-17.txt:        of the red/green matrix originally introduced by Eisen and
biomed/1471-2105-3-17.txt:            majority of genes are colored in green, indicating
biomed/1471-2105-3-17.txt:            ®green (Molecular Probes), a dye that binds
biomed/1471-2105-3-2.txt:            base pairs. Base pairs with a green, black, grey, or
biomed/1471-2105-3-2.txt:            base pairs and base triples are shown in red and green,
biomed/1471-2105-3-2.txt:            pair). The colors green, black, and grey denote base
biomed/1471-2105-3-2.txt:            green confidence rating have a good covariation score
biomed/1471-2105-3-2.txt:            the green "percentage limit" selection at the top of```

4) `grep -n "search" fileName.txt`

input- `grep -n green chapter-1.txt`

output- ```   
            ```

input-  `grep -n "green" chapter-13.4.txt`

output- `719:                twice explored the possibility of obtaining a U.S. green card shortly before his`

*information for command line options were found at...* [geeksforgeeks.org](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

