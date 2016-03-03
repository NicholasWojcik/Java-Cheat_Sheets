# Java String Cheat Sheet

## Methods
* _str1.equals(str2);_---------------- checks to see if the two strings are the same value (not reference)!
* _str1 == str2;_--------------------- checks to see if the two strings are pointed to the same location in memory
* _str1.contains(str2);_-------------- checks to see if str1 has the substring str2 within it
* _str1.toLowerCase();_--------------- returns str1 as an all lowercase string
* _str1.toUpperCase();_--------------- returns str1 as an all uppercase string
* _str1.equalsIgnoreCase(str2);_------ checks to see if str1 is equal to the value of str2, not case sensitive
* _str1.substring(index1, index2);_--- returns a string based on the to indexes choosen, index1 = start, index2 = end
* _str1.length();_-------------------- returns the char length of str1
* _str1.trim();_---------------------- returns a string with the whitespace deleted

## Notes
> StringBuffer is a class that works differently than String.  Whenever a String is manipulated, it returns a brand new String
.  In the case of StringBuffer, it maintains the object.  So if you wish to reverse a string, it is easiest to use the StringBuffer class like
below.
* _StringBuffer_ strBuff = new _StringBuffer_(str1);
* strBuff.reverse().toString();             <-- returns the string reversed