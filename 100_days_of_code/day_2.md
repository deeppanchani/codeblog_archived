# 100 Days Of Code - Day 2 - 22-08-2021
## Topic -Variables and Basic Types 
## Book - C++ Primer
## Notes

Type determine the meaning of the data and operations in our programs. The meaning of even as simple a statement as
```c++
i = i + j;
```
depends on the type of i and j. 

### Primitive Built-in Types
C++ has a set of primitive types that includes
1. Arithmetic Type - It represents **characters, integers, boolean values and floating point number**.
2. void - A special Types - It has no **associated values** and is **most commonly used as the return type of functions** that do not return a value.

**Table: C++: Arithmetic Types**
|Type|Meaning|Minimum Size|
|--|--|--|
|bool|boolean|NA|
|char|character|8 bit|
|wchar_t|wide character|16 bits
|char16_t|Unicode character|16 bits
|char32_t|Unicode character|32 bits
|short|short integer|16 bits
|int|integer|16 bits
|long|long integer|32 bits
|long long|long integer|64 bits
|float|single-precision floating-point|6 significant digits
|double|double-precision floating-point|10 significant digits
|long double|extended-precision floating-point|10 significant digits

**Table: C++: Data Type Range and Size**
<table>
<thead>
<tr>
<th>Type Name</th>
<th>Bytes</th>
<th>Other Names</th>
<th>Range of Values</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong><code>int</code></strong></td>
<td>4</td>
<td><strong><code>signed</code></strong></td>
<td>-2,147,483,648 to 2,147,483,647</td>
</tr>
<tr>
<td><strong><code>unsigned int</code></strong></td>
<td>4</td>
<td><strong><code>unsigned</code></strong></td>
<td>0 to 4,294,967,295</td>
</tr>
<tr>
<td><strong><code>__int8</code></strong></td>
<td>1</td>
<td><strong><code>char</code></strong></td>
<td>-128 to 127</td>
</tr>
<tr>
<td><strong><code>unsigned __int8</code></strong></td>
<td>1</td>
<td><strong><code>unsigned char</code></strong></td>
<td>0 to 255</td>
</tr>
<tr>
<td><strong><code>__int16</code></strong></td>
<td>2</td>
<td><strong><code>short</code></strong>, <strong><code>short int</code></strong>, <strong><code>signed short int</code></strong></td>
<td>-32,768 to 32,767</td>
</tr>
<tr>
<td><strong><code>unsigned __int16</code></strong></td>
<td>2</td>
<td><strong><code>unsigned short</code></strong>, <strong><code>unsigned short int</code></strong></td>
<td>0 to 65,535</td>
</tr>
<tr>
<td><strong><code>__int32</code></strong></td>
<td>4</td>
<td><strong><code>signed</code></strong>, <strong><code>signed int</code></strong>, <strong><code>int</code></strong></td>
<td>-2,147,483,648 to 2,147,483,647</td>
</tr>
<tr>
<td><strong><code>unsigned __int32</code></strong></td>
<td>4</td>
<td><strong><code>unsigned</code></strong>, <strong><code>unsigned int</code></strong></td>
<td>0 to 4,294,967,295</td>
</tr>
<tr>
<td><strong><code>__int64</code></strong></td>
<td>8</td>
<td><strong><code>long long</code></strong>, <strong><code>signed long long</code></strong></td>
<td>-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807</td>
</tr>
<tr>
<td><strong><code>unsigned __int64</code></strong></td>
<td>8</td>
<td><strong><code>unsigned long long</code></strong></td>
<td>0 to 18,446,744,073,709,551,615</td>
</tr>
<tr>
<td><strong><code>bool</code></strong></td>
<td>1</td>
<td>none</td>
<td><strong><code>false</code></strong> or <strong><code>true</code></strong></td>
</tr>
<tr>
<td><strong><code>char</code></strong></td>
<td>1</td>
<td>none</td>
<td>-128 to 127 by default<br><br> 0 to 255 when compiled by using <a href="../build/reference/j-default-char-type-is-unsigned?view=msvc-160" data-linktype="relative-path"><code>/J</code></a></td>
</tr>
<tr>
<td><strong><code>signed char</code></strong></td>
<td>1</td>
<td>none</td>
<td>-128 to 127</td>
</tr>
<tr>
<td><strong><code>unsigned char</code></strong></td>
<td>1</td>
<td>none</td>
<td>0 to 255</td>
</tr>
<tr>
<td><strong><code>short</code></strong></td>
<td>2</td>
<td><strong><code>short int</code></strong>, <strong><code>signed short int</code></strong></td>
<td>-32,768 to 32,767</td>
</tr>
<tr>
<td><strong><code>unsigned short</code></strong></td>
<td>2</td>
<td><strong><code>unsigned short int</code></strong></td>
<td>0 to 65,535</td>
</tr>
<tr>
<td><strong><code>long</code></strong></td>
<td>4</td>
<td><strong><code>long int</code></strong>, <strong><code>signed long int</code></strong></td>
<td>-2,147,483,648 to 2,147,483,647</td>
</tr>
<tr>
<td><strong><code>unsigned long</code></strong></td>
<td>4</td>
<td><strong><code>unsigned long int</code></strong></td>
<td>0 to 4,294,967,295</td>
</tr>
<tr>
<td><strong><code>long long</code></strong></td>
<td>8</td>
<td>none (but equivalent to <strong><code>__int64</code></strong>)</td>
<td>-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807</td>
</tr>
<tr>
<td><strong><code>unsigned long long</code></strong></td>
<td>8</td>
<td>none (but equivalent to <strong><code>unsigned __int64</code></strong>)</td>
<td>0 to 18,446,744,073,709,551,615</td>
</tr>
<tr>
<td><strong><code>enum</code></strong></td>
<td>varies</td>
<td>none</td>
<td></td>
</tr>
<tr>
<td><strong><code>float</code></strong></td>
<td>4</td>
<td>none</td>
<td>3.4E +/- 38 (7 digits)</td>
</tr>
<tr>
<td><strong><code>double</code></strong></td>
<td>8</td>
<td>none</td>
<td>1.7E +/- 308 (15 digits)</td>
</tr>
<tr>
<td><strong><code>long double</code></strong></td>
<td>same as <strong><code>double</code></strong></td>
<td>none</td>
<td>Same as <strong><code>double</code></strong></td>
</tr>
<tr>
<td><strong><code>wchar_t</code></strong></td>
<td>2</td>
<td><strong><code>__wchar_t</code></strong></td>
<td>0 to 65,535</td>
</tr>
</tbody>
</table>

**Arithmetic Type:**
1. Character Type

    The bool type represents the truth values true and false.

    A <code>char</code> is guaranteed to be big enough to hold numeric values corresponding to the characters in the machine’s basic character set.

    A <code>char</code> is the same size as a single machine byte.

    Remaining character types <code>wchar_t, char16_t, and char32_t</code> are used for extended character sets.

    <code>wchar_t</code> type is guaranteed to be large enough to hold any character in the machine’s largest extended  character set.

    <code>char16_t</code> and <code>char32_t</code> are intended for Unicode characters.
1. Integer Type

    <code>long long</code> >= <code>long</code> >= <code>int</code> >= <code>short</code>
1. Floating-point Type

    They represent single-, double-, and extended-precision values.

    <code>float</code> represents one word(32 bits).
    <code>double</code> represents two words(64 bits).
    <code>long double</code> represents either three or four words(96 or 128 bits).

**Signed and Unsigned Types**

Except for bool and the extended character types, the integral typesmay be signed
or unsigned.

<code>signed</code> type represents negative or positive numbers (including zero).
<code>unsigned</code> type represents only values greater than or equal to zero.

<code>int, short, long, long long</code> are all signed by default. We obtain unsigned tye by adding <code>unsigned</code>. For Eg.
```c++
unsigned long variable;
```
Unlike the other integer types, there are three distinct basic character types: 
1. char
1. signed char
1. unsigned char.

<code>char</code> is not the same type as <code>signed char</code>

**A few rules of thumb can be useful in deciding which type to use:**
• Use an unsigned type when you know that the values cannot be negative.

• Use int for integer arithmetic. short is usually too small and, in practice, long often has the same size as int. If your data values are larger than the minimum guaranteed size of an int, then use long long.

• Do not use plain char or bool in arithmetic expressions. Use them only to hold characters or truth values. Computations using char are especially problematic because char is signed on some machines and unsigned on others. If you need a tiny integer, explicitly specify either signed char or unsigned char.

• Use double for floating-point computations; float usually does not have enough precision, and the cost of double-precision calculations versus singleprecision is negligible. In fact, on some machines, double-precision operations are faster than single. The precision offered by long double usually is unnecessary and often entails considerable run-time cost.

### Type Conversions

The type of an object defines the data that an object might contain and what operations that object can perform.

Type conversions happen automatically when we use an object of one type where an object of another type is expected.

```c++
bool b = 42; // b is true
int i = b; // i has value 1
i = 3.14; // i has value 3
double pi = i; // pi has value 3.0
unsigned char c = -1; // assuming 8-bit chars, c has value 255
signed char c2 = 256; // assuming 8-bit chars, the value of c2 is undefined
```

## Exercise
**Exercise 2.1:** What are the differences between int, long, long long, and short? Between an unsigned and a signed type? Between a float and a double?
**Answer 2.1:**
- The difference between int, long, long long, and short is the size of data it stores.
- Unsigned stores number greater than equal to 0. Signed stores all number negative, 0 and positive.
- The difference between floar and double is the amount of precision both has.

**Exercise 2.2:** To calculate a mortgage payment, what types would you use for the rate, principal, and payment? Explain why you selected each type.
**Answer 2.2:**
- Rate <code>float</code>
- Principal <code>long long</code>
- Payment <code>long long</code>

The rate is usually a floating-point number with 4 significant digits. The principal and payment are integral usually less than 1 trillion.
