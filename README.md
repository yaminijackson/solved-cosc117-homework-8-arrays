Download Link: https://assignmentchef.com/product/solved-cosc117-homework-8-arrays
<br>
Review the class examples we discussed this past week and make sure you understand what each command and operation does. Specifically, make sure you understand array creation and manipulation.

For each exercise submit

<ol>

 <li>The Java code file containing the program.</li>

 <li>A Word, LibreOffice, or text file containing at least 3 runs of the program.</li>

</ol>

<h1>2      Exercises</h1>

<ol>

 <li>Create a program that does the following.

  <ul>

   <li>In the main, the program will ask the user for the size of the array. The main will create an array of integers of that size.</li>

   <li>The main will call the method PopulateArray(<strong>int</strong>[] A)</li>

  </ul></li>

</ol>

which will ask the user for each entry of the array one by one and insert the input values into the array.

<ul>

 <li>The main will then call a method to print the array out to the screen with some spaces between the entries. We will update the method we developed in class. This method will take the array as a parameter but it will also take a width for the amount of space to use for each entry. The method header will look like the following,</li>

</ul>

<strong>public static void </strong>PrintArray(<strong>int</strong>[] A, <strong>int </strong>width)

For this method you will be using a printf instead of a print. Recall that with an integer you use a d in the <em>tag </em>to format the integer. So the following line System.out.printf(“%5d”, A[i]);

will print the <em>i<sup>th </sup></em>entry of <em>A </em>with 5 spaces. You will need to update this so that the input width is used in place of the 5.

<ul>

 <li>The main should then call a method ManipulateArray(<strong>int</strong>[] A)</li>

</ul>

which does the following to each entry in the array. If the entry is even then the entry is replaced by half its value, if the entry is evenly divisible by 3 then the entry is replaced with one third its value, if the entry is neither divisible by 2 or 3 then 5 is added to the entry.

<ul>

 <li>The main should then print out the contents of the array.</li>

 <li>The main should then call the manipulate and the print methods two more times.</li>

</ul>

A run of the program is below.

Input Array Size: 5

Input entry 1: 1

Input entry 2: 2

Input entry 3: 3

Input entry 4: 4

Input entry 5: 5

1       2       3       4       5

6       1       1        2 10

3       6       6       1       5

1       3       3        6 10

<ol start="2">

 <li>Recall the Nifty sequence that takes a number and if it is even it will divide it by 2 and if it is odd it will multiply by 3 and add 1. As we discussed before the sequence always seems to hit one at some point and then we stop the sequence. This exercise will take an input number from the user and instead of just printing the sequence out it will store the sequence in an array. Since the length of the sequence differs depending on the first number we will need to calculate the sequence first to determine its length, then create an array of just the right size, and then put the sequence into the array.</li>

</ol>

Create a program that does the following.

<ul>

 <li>In the main, the program will ask the user for the first number.</li>

 <li>The main then will call the method <strong>public static int </strong>NiftySequenceLength(<strong>int </strong>n)</li>

</ul>

that will return the length of the sequence what begins with the number <em>n</em>.

<ul>

 <li>The main then creates the array of the correct size, loads <em>n </em>into the first position and then calls,</li>

</ul>

<strong>public static void </strong>PopulateArray(<strong>int</strong>[] A)

which loads the sequence into the array.

<ul>

 <li>Have the main call a print array method to print out the array. You can, of course, use the array printer that you wrote in the previous exercise.</li>

 <li>Have the program call two more methods that you will write. One of these is to count the number of even numbers in the list and the other is to count the odd numbers in the list. The headers for these will look like,</li>

</ul>

<strong>public static int </strong>CountEvens(<strong>int</strong>[] A) <strong>public static int </strong>CountOdds(<strong>int</strong>[] A)

Have the main print these values out.

A run of the program is below.

<strong>Program Run:</strong>

Input n: 12

12       6         3 10           5 16         8       4       2      1

Number of even numbers in the list: 7

Number of odd numbers in the list: 3

<ol start="3">

 <li>Below is the start of a program that creates a random one-dimensional array of a size that is input by the user and a maximum entry size also specified by the user. The program also takes in an input of an integer countdiv which is a number used in the two counting functions described below. After the code segment and run there are instructions on what functions you should create. The main program and functions that are already written are not to be altered, you will simply be adding functions to the program.</li>

</ol>

<strong>import </strong>java.util.Scanner;

<strong>public class </strong>Lab08_03 {

&lt;&lt;&lt; INSERT NEW FUNCTIONS HERE &gt;&gt;&gt;

<strong>public static void </strong>main(String[] args) {

Scanner keyboard = <strong>new </strong>Scanner(System.in); System.out.print(“Input the array size: “); <strong>int </strong>arraySize = keyboard.nextInt(); System.out.print(“Input max entry size: “); <strong>int </strong>entrysize = keyboard.nextInt();

System.out.print(“Input the count division: “); <strong>int </strong>countdiv = keyboard.nextInt();

<strong>int </strong>intArray[] = <strong>new int</strong>[arraySize];

PopulateArray(intArray, entrysize);

PrintArray(intArray, 4);

System.out.println(“The sum of the array is = ” + SumArray(intArray));

System.out.println(“The average of the array is = ” + AvgArray(intArray));

System.out.println(“The maximum of the array is = ” + MaxArray(intArray));

System.out.println(“The minimum of the array is = ” + MinArray(intArray));

System.out.println(“The number less than ” + countdiv + ” in the array is = ”

+ CountLessArray(intArray, countdiv));

System.out.println(“The number greater than ” + countdiv + ” in the array is = ”

+ CountGreaterArray(intArray, countdiv));

System.out.println(“The variance of the array is = ” + VarianceArray(intArray));

System.out.println(“The standard deviation of the array is = ” + StandardDeviationArray(intArray)

);

System.out.println();

PrintArrayBarChart(intArray); System.out.println();

<strong>int</strong>[] B = ReverseArray(intArray);

PrintArray(intArray, 4);

PrintArray(B, 4);

}

}

<strong>Program Run:</strong>

Input the array size: 20

Input max entry size: 50

Input the count division: 15

44 39                                      9 50 32 33 22 10 37 18 33 10 47 37 48 31 20                                       2 21 18

The sum of the array is = 561

The average of the array is = 28.05

The maximum of the array is = 50

The minimum of the array is = 2

The number less than 15 in the array is = 4

The number greater than 15 in the array is = 16

The variance of the array is = 204.89210526315787

The standard deviation of the array is = 14.314052719728187

********************************************

***************************************

*********

**************************************************

********************************

*********************************

**********************

**********

*************************************

******************

*********************************

**********

***********************************************

*************************************

************************************************

*******************************

********************

**

*********************

******************

44 39                                      9 50 32 33 22 10 37 18 33 10 47 37 48 31 20                                       2 21 18

18 21                                      2 20 31 48 37 47 10 33 18 37 10 22 33 32 50                                       9 39 44

The functions you are to create and what they do are described below.

(a) <strong>public static void </strong>PopulateArray(<strong>int</strong>[] A, <strong>int </strong>n)

This function will take in an array and integer <em>n </em>and populate the array with random numbers between 1 and <em>n</em>.

<h2>(b) <strong>public static void </strong>PrintArray(<strong>int</strong>[] Arr, <strong>int </strong>width)</h2>

This method will take the array as a parameter but it will also take a width for the amount of space to use for each entry. You will simply need to use the one you created earlier.

<h2>(c) <strong>public static void </strong>PrintArrayBarChart(<strong>int</strong>[] Arr)</h2>

This function prints a bar chart of the array entries. The bars are horizontal and the number of * matches the array entry.

<ul>

 <li><strong>public static int </strong>SumArray(<strong>int</strong>[] Arr)</li>

</ul>

This function calculates and returns the sum of the array entries.

<ul>

 <li><strong>public static double </strong>AvgArray(<strong>int</strong>[] Arr)</li>

</ul>

This function calculates and returns the average of the array entries. If the size of the array is less than one return 0.

<ul>

 <li><strong>public static double </strong>VarianceArray(<strong>int</strong>[] Arr)</li>

</ul>

This function calculates and returns the variance of the array entries. The variance of a list of numbers is defined to be where <em>x<sub>i </sub></em>represents the <em>i<sup>th </sup></em>entry in the array and <em>µ </em>is the average (or mean) of the array entries. The sum is taken over all array entries and <em>n </em>is the size of the array. If the size of the array is less than two the function should return 0.

<h2>(g) <strong>public static double </strong>StandardDeviationArray(<strong>int</strong>[] Arr)</h2>

This function calculates and returns the standard deviation of the array entries. The standard deviation of a list of numbers is defined to be the square root of the variance. As with the variance, if the size of the array is less than two return 0.

<ul>

 <li><strong>public static int </strong>MaxArray(<strong>int</strong>[] Arr)</li>

</ul>

This function finds and returns the maximum value of the array.

<ul>

 <li><strong>public static int </strong>MinArray(<strong>int</strong>[] Arr)</li>

</ul>

This function finds and returns the minimum value of the array.

<ul>

 <li><strong>public static int </strong>CountLessArray(<strong>int</strong>[] Arr, <strong>int </strong>n)</li>

</ul>

This function finds and returns the number of array entries that are strictly less than <em>n</em>.

<ul>

 <li><strong>public static int </strong>CountGreaterArray(<strong>int</strong>[] Arr, <strong>int </strong>n)</li>

</ul>

This function finds and returns the number of array entries that are strictly greater than <em>n</em>.

<h2>(l) <strong>public static int</strong>[] ReverseArray(<strong>int</strong>[] Arr)</h2>

This function returns an array of the same size as the one input with its entries in reverse order. Note that the return type is an array of integers int[]. To make a method return an array you need to create a new array inside the method and then return it at the end. Since this array has the same size as the one coming in as a parameter we need to use Arr.length as the size of the new array. The shell to this method is as follows.

<strong>public static int</strong>[] ReverseArray(<strong>int</strong>[] Arr) { <strong>int </strong>B[] = <strong>new int</strong>[Arr.length];

<h2>&lt; Insert code that will store the reverse of the array Arr in B. &gt;</h2>

<strong>return </strong>B;

}

Be careful not to alter the contents of Arr since this will alter the contents of the array created in the main and we do not want to do that.

<h1>3         Challenge Exercise: The Vigen`ere Cipher</h1>

Challenge Exercises are optional, they will be graded as extra credit.

The Vigen`ere cipher was developed in the mid sixteenth century by Blaise de Vigen`ere. When Vigen`ere was twenty six years old he went on a two-year diplomatic mission to Rome. There is where he was first exposed to the world of cryptography. Building on the work of Leon Battista Alberti(1404–1472) (often called the Father of Western Cryptography), Johannes Trithemius, and Giovanni Porta, Vigen`ere developed several cryptographic methods and steganographic techniques. In 1585 he published <em>Traict`e des Chiffres</em>, which contained his contributions to the field. Vigen`ere developed much more sophisticated ciphers then the standard repeated keyword cipher we will discuss here. We will briefly discuss some of the autokey ciphers that Vigen`ere published in the Traict`e des Chiffres, which can be more difficult to break than the classical repeated keyword.

Alberti was one the leading figures of the Renaissance; a painter, composer, poet and philosopher. He was also the author of the first scientific analysis of perspective, a treatise on the housefly, and a funeral oration for his dog. He is probably best known as an architect, having designed Rome’s first Trevi Fountain and having written “De Re Aedificatoria”, the first printed book on architecture, which acted as a catalyst for the transition from Gothic to Renaissance design.<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>

The Vigen`ere cipher is a polyalphabetic cipher which is a variation of the Caesar shift cipher. As the name implies it uses several different alphabetic substitutions in place of the one, as in the monoalphabetic ciphers.

The Vigen`ere cipher was one of those “quantum leaps” in cryptography, of which there are several in history, where it seems that a completely secure method of encryption had been found. The Vigen`ere cipher was considered to be unbreakable, and it achieved the title of the <em>chiffre ind´echiffrable</em>. It was not until 1863, nearly 300 years after its creation, when F. W. Kasiski found a method for cryptanalyzing the cipher and later the method of coincidence analysis made the determination of the keyword length even easier.

The Vigen`ere cipher encryption is implemented as follows,

<ol>

 <li>A keyword is chosen for the cipher, this is the key to both encryption and decryption.</li>

 <li>Each letter is converted to a shift value using the standard A–Z as 0–25, as in the chart below. The keyword then becomes a shift vector.</li>

</ol>

For example, if the keyword is VIGENERE then the shift vector is (21<em>,</em>8<em>,</em>6<em>,</em>4<em>,</em>13<em>,</em>4<em>,</em>17<em>,</em>4).

<ol start="3">

 <li>The plaintext message is written out character for character and the keyword (or shift vector) is written below it, character for character and the keyword is repeated as many times as is needed to cover the message.</li>

 <li>Each character in the plaintext message is shifted by the amount as its corresponding keyword letter to create the ciphertext.</li>

</ol>

Table 1: Vigen`ere Cipher Shift Coding

<table width="438">

 <tbody>

  <tr>

   <td width="57"><strong>Letter</strong></td>

   <td width="29">A</td>

   <td width="29">B</td>

   <td width="29">C</td>

   <td width="29">D</td>

   <td width="29">E</td>

   <td width="29">F</td>

   <td width="29">G</td>

   <td width="29">H</td>

   <td width="29">I</td>

   <td width="30">J</td>

   <td width="29">K</td>

   <td width="29">L</td>

   <td width="29">M</td>

  </tr>

  <tr>

   <td width="57"><strong>Shift</strong></td>

   <td width="29">0</td>

   <td width="29">1</td>

   <td width="29">2</td>

   <td width="29">3</td>

   <td width="29">4</td>

   <td width="29">5</td>

   <td width="29">6</td>

   <td width="29">7</td>

   <td width="29">8</td>

   <td width="30">9</td>

   <td width="29">10</td>

   <td width="29">11</td>

   <td width="29">12</td>

  </tr>

  <tr>

   <td width="57"><strong>Letter</strong></td>

   <td width="29">N</td>

   <td width="29">O</td>

   <td width="29">P</td>

   <td width="29">Q</td>

   <td width="29">R</td>

   <td width="29">S</td>

   <td width="29">T</td>

   <td width="29">U</td>

   <td width="29">V</td>

   <td width="30">W</td>

   <td width="29">X</td>

   <td width="29">Y</td>

   <td width="29">Z</td>

  </tr>

  <tr>

   <td width="57"><strong>Shift</strong></td>

   <td width="29">13</td>

   <td width="29">14</td>

   <td width="29">15</td>

   <td width="29">16</td>

   <td width="29">17</td>

   <td width="29">18</td>

   <td width="29">19</td>

   <td width="29">20</td>

   <td width="29">21</td>

   <td width="30">22</td>

   <td width="29">23</td>

   <td width="29">24</td>

   <td width="29">25</td>

  </tr>

 </tbody>

</table>

The decryption process is the same except that the shift done in the last step is reversed to take the cuphertext back to the plaintext.

<strong>Example: </strong>Lets say that we want to send the message,

Meet me at Cool Beans tomorrow afternoon.

First we convert the message as follows, we convert it to all uppercase,

MEET ME AT COOL BEANS TOMORROW AFTERNOON.

then we remove anything that is not an alphabetic character,

MEETMEATCOOLBEANSTOMORROWAFTERNOON

Lets say that we use the key

coffee

We do the same to the key as we did with the message so it gets converted to

COFFEE

We then convert the characters to numbers, A to 0, B to 1, C to 2, …, Z to 25. So our message is coded as

12 4 4 19 12 4 0 19 2 14 14 11 1 4 0 13 18 19 14 12 14 17 17 14 22 0 5 19 4 17 13 14 14 13

We do the same with the key.

2 14 5 5 4 4

Now we repeat the key so that it has the same number of numbers as the message, and we place it next to the message. We then add entry by entry and take the result mod 26. The table below shows the process.

<table width="228">

 <tbody>

  <tr>

   <td width="72"><strong>Message</strong></td>

   <td width="43"><strong>Key</strong></td>

   <td width="46"><strong>Sum</strong></td>

   <td width="67"><strong>Mod 26</strong></td>

  </tr>

  <tr>

   <td width="72">12</td>

   <td width="43">2</td>

   <td width="46">14</td>

   <td width="67">14</td>

  </tr>

  <tr>

   <td width="72">4</td>

   <td width="43">14</td>

   <td width="46">18</td>

   <td width="67">18</td>

  </tr>

  <tr>

   <td width="72">4</td>

   <td width="43">5</td>

   <td width="46">9</td>

   <td width="67">9</td>

  </tr>

  <tr>

   <td width="72">19</td>

   <td width="43">5</td>

   <td width="46">24</td>

   <td width="67">24</td>

  </tr>

  <tr>

   <td width="72">12</td>

   <td width="43">4</td>

   <td width="46">16</td>

   <td width="67">16</td>

  </tr>

  <tr>

   <td width="72">4</td>

   <td width="43">4</td>

   <td width="46">8</td>

   <td width="67">8</td>

  </tr>

  <tr>

   <td width="72">0</td>

   <td width="43">2</td>

   <td width="46">2</td>

   <td width="67">2</td>

  </tr>

  <tr>

   <td width="72">19</td>

   <td width="43">14</td>

   <td width="46">33</td>

   <td width="67">7</td>

  </tr>

  <tr>

   <td width="72">2</td>

   <td width="43">5</td>

   <td width="46">7</td>

   <td width="67">7</td>

  </tr>

  <tr>

   <td width="72">14</td>

   <td width="43">5</td>

   <td width="46">19</td>

   <td width="67">19</td>

  </tr>

  <tr>

   <td width="72">14</td>

   <td width="43">4</td>

   <td width="46">18</td>

   <td width="67">18</td>

  </tr>

  <tr>

   <td width="72">11</td>

   <td width="43">4</td>

   <td width="46">15</td>

   <td width="67">15</td>

  </tr>

  <tr>

   <td width="72">1</td>

   <td width="43">2</td>

   <td width="46">3</td>

   <td width="67">3</td>

  </tr>

  <tr>

   <td width="72">4</td>

   <td width="43">14</td>

   <td width="46">18</td>

   <td width="67">18</td>

  </tr>

  <tr>

   <td width="72">0</td>

   <td width="43">5</td>

   <td width="46">5</td>

   <td width="67">5</td>

  </tr>

  <tr>

   <td width="72"><strong>Message</strong></td>

   <td width="43"><strong>Key</strong></td>

   <td width="46"><strong>Sum</strong></td>

   <td width="67"><strong>Mod 26</strong></td>

  </tr>

  <tr>

   <td width="72">13</td>

   <td width="43">5</td>

   <td width="46">18</td>

   <td width="67">18</td>

  </tr>

  <tr>

   <td width="72">18</td>

   <td width="43">4</td>

   <td width="46">22</td>

   <td width="67">22</td>

  </tr>

  <tr>

   <td width="72">19</td>

   <td width="43">4</td>

   <td width="46">23</td>

   <td width="67">23</td>

  </tr>

  <tr>

   <td width="72">14</td>

   <td width="43">2</td>

   <td width="46">16</td>

   <td width="67">16</td>

  </tr>

  <tr>

   <td width="72">12</td>

   <td width="43">14</td>

   <td width="46">26</td>

   <td width="67">0</td>

  </tr>

  <tr>

   <td width="72">14</td>

   <td width="43">5</td>

   <td width="46">19</td>

   <td width="67">19</td>

  </tr>

  <tr>

   <td width="72">17</td>

   <td width="43">5</td>

   <td width="46">22</td>

   <td width="67">22</td>

  </tr>

  <tr>

   <td width="72">17</td>

   <td width="43">4</td>

   <td width="46">21</td>

   <td width="67">21</td>

  </tr>

  <tr>

   <td width="72">14</td>

   <td width="43">4</td>

   <td width="46">18</td>

   <td width="67">18</td>

  </tr>

  <tr>

   <td width="72">22</td>

   <td width="43">2</td>

   <td width="46">24</td>

   <td width="67">24</td>

  </tr>

  <tr>

   <td width="72">0</td>

   <td width="43">14</td>

   <td width="46">14</td>

   <td width="67">14</td>

  </tr>

  <tr>

   <td width="72">5</td>

   <td width="43">5</td>

   <td width="46">10</td>

   <td width="67">10</td>

  </tr>

  <tr>

   <td width="72">19</td>

   <td width="43">5</td>

   <td width="46">24</td>

   <td width="67">24</td>

  </tr>

  <tr>

   <td width="72">4</td>

   <td width="43">4</td>

   <td width="46">8</td>

   <td width="67">8</td>

  </tr>

  <tr>

   <td width="72">17</td>

   <td width="43">4</td>

   <td width="46">21</td>

   <td width="67">21</td>

  </tr>

  <tr>

   <td width="72">13</td>

   <td width="43">2</td>

   <td width="46">15</td>

   <td width="67">15</td>

  </tr>

  <tr>

   <td width="72">14</td>

   <td width="43">14</td>

   <td width="46">28</td>

   <td width="67">2</td>

  </tr>

  <tr>

   <td width="72">14</td>

   <td width="43">5</td>

   <td width="46">19</td>

   <td width="67">19</td>

  </tr>

  <tr>

   <td width="72">13</td>

   <td width="43">5</td>

   <td width="46">18</td>

   <td width="67">18</td>

  </tr>

 </tbody>

</table>

We then take the last column of numbers and convert these to letters again using the 0 to A, 1 to B, 2 to C, …, 25 to Z. So our ciphertext is

OSJYQICHHTSPDSFSWXQATWVSYOKYIVPCTS

If we wanted to decrypt this ciphertext we would simply reverse the process and subtract the key from the ciphertext letters.

For this exercise you will construct a program that will encrypt and decrypt messages using the Vigen`ere

Cipher. First construct the following methods,

<h2>1. <strong>public static char</strong>[] ProcessMessage(String message)</h2>

This method will take in a string and return an array of characters that are all uppercase and any characters removed that are not alphabetic. So the input of Meet me at Cool Beans tomorrow afternoon. will get converted to an array of the characters

MEETMEATCOOLBEANSTOMORROWAFTERNOON

One command that will come in handy here is in the Character class. If ch is a character then the command Character.isAlphabetic(ch) will return true if ch is an alphabetic character and false otherwise.

<h2>2. <strong>public static int</strong>[] ConvertCharArrayToIntegerArray(<strong>char</strong>[] A)</h2>

This will convert an array of characters to an array of integers using A to 0, B to 1, C to 2, …, Z to

25.

<h2>3. <strong>public static char</strong>[] ConvertIntegerArrayToCharArray(<strong>int</strong>[] A)</h2>

This will convert an array of integers to an array of characters using 0 to A, 1 to B, 2 to C, …, 25 to Z.

<ol start="4">

 <li><strong>public static </strong>String ConvertCharArrayToString(<strong>char</strong>[] A)</li>

</ol>

This will convert an array of characters to a string.

<h2>5. <strong>public static int</strong>[] RepeatArray(<strong>int</strong>[] A, <strong>int </strong>newLength)</h2>

This will take an array of integers and make a new array of the length newLength and will put the array entries of A into the new array repeating A as many times as needed. For example, if we start with the array

<table width="120">

 <tbody>

  <tr>

   <td width="23">3</td>

   <td width="23">7</td>

   <td width="29">13</td>

   <td width="23">4</td>

   <td width="23">2</td>

  </tr>

 </tbody>

</table>

and give a new size of 18 the result will be the array,

<table width="433">

 <tbody>

  <tr>

   <td width="23">3</td>

   <td width="23">7</td>

   <td width="29">13</td>

   <td width="23">4</td>

   <td width="23">2</td>

   <td width="23">3</td>

   <td width="23">7</td>

   <td width="29">13</td>

   <td width="23">4</td>

   <td width="23">2</td>

   <td width="23">3</td>

   <td width="23">7</td>

   <td width="29">13</td>

   <td width="23">4</td>

   <td width="23">2</td>

   <td width="23">3</td>

   <td width="23">7</td>

   <td width="29">13</td>

  </tr>

 </tbody>

</table>

<h2>6. <strong>public static int</strong>[] VigenereEncrypt(<strong>int</strong>[] Message, <strong>int</strong>[] Key)</h2>

This will take the two integer arrays (assumed to be the same length), add them together entry by entry, modulo 26, and return the new array.

<h2>7. <strong>public static int</strong>[] VigenereDecrypt(<strong>int</strong>[] Cipher, <strong>int</strong>[] Key)</h2>

This will take the two integer arrays (assumed to be the same length), subtract the Key from the Cipher, modulo 26, and return the new array. Here you need to be careful because % does not work the way you want it to with negative numbers.

Now write a main program that uses these to encrypt and decrypt a message using the Vigen`ere Cipher. The program should first ask the user if they want to encrypt or decrypt. Then it will ask for the message or ciphertext and key. It will then convert the message or ciphertext to uppercase with only characters being used. Same for the key. It will then convert the characters to arrays of integers, do the encryption or decryption, and then convert the result to a string and print it to the screen. Some examples are below,

Encode or Decode (E/D): e

Input the message: Meet me at Cool Beans tomorrow afternoon.

Input the keyword: coffee Ciphertext: OSJYQICHHTSPDSFSWXQATWVSYOKYIVPCTS

Encode or Decode (E/D): d Input the ciphertext: OSJYQICHHTSPDSFSWXQATWVSYOKYIVPCTS Input the keyword: coffee Plaintext: MEETMEATCOOLBEANSTOMORROWAFTERNOON

Encode or Decode (E/D): e

Input the message: Not much of a challenge.

Input the keyword: Vigenere Ciphertext: IWZQHGYSAIILNPCIIOK

<a href="#_ftnref1" name="_ftn1">[1]</a> The Black Chamber by Simon Singh (2015) http://www.simonsingh.net/The_Black_Chamber/