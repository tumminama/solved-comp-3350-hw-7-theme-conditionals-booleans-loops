Download Link: https://assignmentchef.com/product/solved-comp-3350-hw-7-theme-conditionals-booleans-loops
<br>
<strong><em> </em></strong>

<ol>

 <li>Draft a program that scans an array to determine the first positive EVEN number in the array. If a positive value is found, the program should print “positive even number found” and the value.  If no positive EVEN value is found in the array, the program should print “no positive even number found.” Submit list file and show the runs for the following data items:

  <ol>

   <li>all negative even values</li>

   <li>all positive odd values</li>

   <li>mixed negative and positive values which are odd and even (two different examples with odd and even numbers at different indices)</li>

  </ol></li>

</ol>




a.




b.




c.Mix1







c.Mix2




<ol start="2">

 <li>Write a program which encodes any string using the XOR instruction. Test it using your &lt;first name last name&gt; in the data segment to produce cipher text and then decode using the program to get plain text.  Use the last three digits of your student id as the key.  Print plane text from the data segment, print the cipher text, and then print the plain text upon execution.  What are the strengths and weaknesses of this encryption method?  Can you think of another way doing such encryption?  What are the strengths and weaknesses of your method? <strong><em> </em></strong></li>

</ol>




<strong><em> </em></strong>




Strengths: Hard to find out original text at one glance

Weaknesses: The length of cipher text is the same with original text, the original text can be guessed in long run. Using only one key will also increase the risk.




Other method: One time pad encryption

Strengths: Every key is one-time used, more secure.

Weakness: Cannot be decode if losing the key pad.

<ol start="3">

 <li>Implement the following two pseudo-codes in assembly language (assume signed numbers). Declare Apple and Pear as word sized variables. Test the program for input data sets listed below and print values assigned to Apple and Pear. Submit list file and show output for all input data sets.</li>

</ol>




<ol>

 <li>if ( (cx = bx) AND (cx &gt;= val1) )</li>

</ol>

Apple = 1;

Else

Apple = 0;




<ol>

 <li>if ( (bx = cx)  OR  (cx &gt;= val1) )</li>

</ol>

Pear = 1;

Else

Pear = 0;







<strong>            <u>Input test data</u> </strong>




<table width="121">

 <tbody>

  <tr>

   <td width="37"><strong>CX </strong></td>

   <td width="37"><strong>BX </strong></td>

   <td width="46"><strong>Val1 </strong></td>

  </tr>

  <tr>

   <td width="37">0</td>

   <td width="37">0</td>

   <td width="46">0</td>

  </tr>

  <tr>

   <td width="37">0</td>

   <td width="37">0</td>

   <td width="46">1</td>

  </tr>

  <tr>

   <td width="37">0</td>

   <td width="37">1</td>

   <td width="46">0</td>

  </tr>

  <tr>

   <td width="37">0</td>

   <td width="37">1</td>

   <td width="46">1</td>

  </tr>

  <tr>

   <td width="37">1</td>

   <td width="37">0</td>

   <td width="46">0</td>

  </tr>

  <tr>

   <td width="37">1</td>

   <td width="37">0</td>

   <td width="46">1</td>

  </tr>

  <tr>

   <td width="37">1</td>

   <td width="37">1</td>

   <td width="46">0</td>

  </tr>

  <tr>

   <td width="37">1</td>

   <td width="37">1</td>

   <td width="46">1</td>

  </tr>

 </tbody>

</table>

000

001

010

011

100

101

110

111

<ol start="4">

 <li>Draw the stack (pencil-paper or wordàpdf) at different points of the main and subroutine to show your understanding of the call and return functions.</li>

</ol>




Main PROC

4040040          call FloatAdd 4040046           mov eax, ebx

…

…




FloatAdd  PROC

4041020          Push ecx

4041024          Push ebx

4041028          mov eax, edx

…

…

404A030         Pop ebx

404A032         Pop ecx

404A034         ret

FloatAdd ENDP




























<table width="220">

 <tbody>

  <tr>

   <td colspan="2" width="152">Before call to FloatAdd</td>

   <td rowspan="2" width="68"> </td>

  </tr>

  <tr>

   <td width="58">OFFSET</td>

   <td width="94"> </td>

  </tr>

  <tr>

   <td colspan="2" width="152"> </td>

   <td width="68">ESP</td>

  </tr>

  <tr>

   <td width="58"></td>

   <td width="94"></td>

   <td width="68"></td>

  </tr>

 </tbody>

</table>

<table width="220">

 <tbody>

  <tr>

   <td colspan="4" width="160">00000FF0        00000000</td>

   <td rowspan="4" width="60">  </td>

  </tr>

  <tr>

   <td colspan="2" width="105">EIP = 04040040</td>

   <td colspan="2" width="55"> </td>

  </tr>

  <tr>

   <td colspan="3" width="142">After call to FloatAdd</td>

   <td rowspan="2" width="18"> </td>

  </tr>

  <tr>

   <td width="58">OFFSET</td>

   <td colspan="2" width="84"> </td>

  </tr>

  <tr>

   <td colspan="4" width="160"> </td>

   <td width="60">ESP</td>

  </tr>

  <tr>

   <td width="58"></td>

   <td width="47"></td>

   <td width="37"></td>

   <td width="18"></td>

   <td width="59"></td>

  </tr>

 </tbody>

</table>

<table width="160">

 <tbody>

  <tr>

   <td colspan="2" width="160">00000FF0        00000000</td>

  </tr>

  <tr>

   <td width="105">EIP = 04041020</td>

   <td width="55"> </td>

  </tr>

 </tbody>

</table>




After Push ecx

OFFSET

00001000

00000FFC       04040046

00000FF8        (ecx)                ESP

00000FF4        00000000

00000FF0        00000000




After Push ebx

OFFSET

00001000

00000FFC       04040046

00000FF8        (ecx)

00000FF4        (ebx)               ESP

00000FF0        00000000




After Pop ebx

OFFSET

00001000

00000FFC       04040046

00000FF8        (ecx)                ESP

00000FF4        00000000

00000FF0        00000000




After Pop ecx

OFFSET

00001000                                ESP

00000FFC       04040046

00000FF8        00000000

<table width="160">

 <tbody>

  <tr>

   <td width="96">00000FF4</td>

   <td width="64">00000000</td>

  </tr>

  <tr>

   <td width="96">00000FF0</td>

   <td width="64">00000000</td>

  </tr>

 </tbody>

</table>

<table width="220">

 <tbody>

  <tr>

   <td width="58">After Re</td>

   <td width="24">turn</td>

   <td rowspan="2" width="138"> </td>

  </tr>

  <tr>

   <td width="58">OFFSET</td>

   <td width="24"> </td>

  </tr>

  <tr>

   <td width="58"> </td>

   <td colspan="2" width="162">ESP</td>

  </tr>

 </tbody>

</table>

<table width="160">

 <tbody>

  <tr>

   <td colspan="2" width="160">00000FF0        00000000</td>

  </tr>

  <tr>

   <td width="105">EIP = 04040046</td>

   <td width="55"> </td>

  </tr>

 </tbody>

</table>











