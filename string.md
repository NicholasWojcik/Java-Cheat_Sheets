# Java String Cheat Sheet

## Methods
* **str1.equals(str2);**---------------------- checks to see if the two strings are the same value (not reference)
* **str1 == str2;**----------------------------- checks to see if the two strings are pointed to the same location in memory
* **str1.contains(str2);**------------------- checks to see if str1 has the substring str2 within it
* **str1.toLowerCase();**------------------ returns str1 as an all lowercase string
* **str1.toUpperCase();**------------------ returns str1 as an all uppercase string
* **str1.equalsIgnoreCase(str2);**------ checks to see if str1 is equal to the value of str2, not case sensitive
* **str1.substring(index1, index2);**--- returns a string based on the to indexes choosen, index1 = start, index2 = end
* **str1.length();**---------------------------- returns the char length of str1
* **str1.trim();**-------------------------------- returns a string with the whitespace deleted

## Notes
> StringBuffer is a class that works differently than String.  Whenever a String is manipulated, it returns a brand new String.  In the case
of StringBuffer, it maintains the object.  So if you wish to reverse a string, it is easiest to use the StringBuffer class like
below.

''' Java
StringBuffer strBuff = new StringBuffer(str1);
strBuff.reverse().toString();
'''