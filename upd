 1. Value Types
Stored directly in stack memory.
Hold actual data.
Copying a value type creates a new copy.
Examples: int, float, bool, struct, enum

int x = 10;
int y = x; // y is a copy of x

static void ChangeValue(int x)
{
    x =  200;
    Console.WriteLine(x);
}
static void Main(string[] args)
{
    int i = 100;
    Console.WriteLine(i); 
    ChangeValue(i);   
    Console.WriteLine(i);
}
100


2. Reference Types
Stored in heap memory, but a reference (pointer) is kept on the stack.
Copying a reference type copies the reference, not the object.
Examples: class, interface, delegate, string, array

class Person { public string Name; }

Person p1 = new Person();
Person p2 = p1; // p2 and p1 reference the same object

static void ChangeReferenceType(Student std2)
{
    std2.StudentName = "Steve";
}

static void Main(string[] args)
{
    Student std1 = new Student();
    std1.StudentName = "Bill";
    
    ChangeReferenceType(std1);

    Console.WriteLine(std1.StudentName);
}

3. It is a process that converts a Value Type variable into a Reference Type variable
int num = 5;
object obj = num; // boxing

// Boxing and Unboxing in C#

using System;

public class Geeks 
{
	public static void Main(string[] args)
	{
		// Value type variable
		int n = 357; 

		// Boxing
		object box = n; 

		Console.WriteLine("Boxed value: " + box);

		// Unboxing
		int unbox = (int)box; 
		Console.WriteLine("Unboxed value: " + unbox);
	}
}

Boxed value: 357
Unboxed value: 357

4.Extracts the value type from a boxed object.

Requires explicit casting.
object obj = 5;
int num = (int)obj; // unboxing

// C# implementation to demonstrate
// the Unboxing
using System;
class Geeks
 {

    static public void Main()
    {

        // assigned int value
        // 23 to num
        int num = 23;

        // boxing
        object box = num;

        // unboxing
        int unbox = (int)box;
    
     System.Console.WriteLine("Value of box: " + box);
	 System.Console.WriteLine("Value of unbox: " + unbox);
    }
}

Value of box: 23
Value of unbox: 23

5.  ref Keyword
Passes a variable by reference, both for input and output.

The value must be initialized before passing.

TestRef t = new TestRef();
t.Something = "Foo";
DoSomething(ref t);

void DoSomething(ref TestRef x)
{
  x = new TestRef();
  x.Something = "Not just a changed TestRef, but a completely different TestRef object";
}

6.out Keyword
Also passes by reference, but only for output.

Variable does not need to be initialized before being passed.

// C# program to illustrate the
// concept of out parameter
using System;

class GFG {

	// Main method
	static public void Main()
	{

		// Declaring variable
		// without assigning value
		int i;

		// Pass variable i to the method
		// using out keyword
		Addition(out i);

		// Display the value i
		Console.WriteLine("The addition of the value is: {0}", i);
	}

	// Method in which out parameter is passed
	// and this method returns the value of 
	// the passed parameter
	public static void Addition(out int i)
	{
		i = 30;
		i += i;
	}
}
The addition of the value is: 60

7. const Keyword
Compile-time constant.

Must be initialized at the time of declaration.

Can't be changed afterward.

// C# program to illustrate the
// use of const keyword
using System;

class GFG {

	// Constant fields
	public const int myvar = 10;
	public const string str = "GeeksforGeeks";

	// Main method
	static public void Main()
	{

		// Display the value of Constant fields
		Console.WriteLine("The value of myvar: {0}", myvar);
		Console.WriteLine("The value of str: {0}", str);
	}
}


The value of myvar: 10
The value of str: GeeksforGeeks

 8. readonly Keyword
Value is assigned at declaration or in constructor.

Useful when value is determined at runtime.

// C# program to illustrate 
// how to create a readonly field 
using System; 

class GFG { 

	// readonly variables 
	public readonly string str1; 
	public readonly string str2; 

	// Readonly variable 
	// This variable is 
	// initialized at declaration time 
	public readonly string str3 = "gfg"; 

	// The values of the readonly 
	// variables are assigned 
	// Using constructor 
	public GFG(string a, string b) 
	{ 

		str1 = a; 
		str2 = b; 
		Console.WriteLine("Display value of string 1 {0}, "
						+ "and string 2 {1}", str1, str2); 
	} 

	// Main method 
	static public void Main() 
	{ 
		GFG ob = new GFG("GeeksforGeeks", "GFG"); 
	} 
} 
Display value of string 1 GeeksforGeeks, and string 2 GFG


 9. String Immutability
Strings in C# are immutable.

Any operation like Replace, Substring creates a new string.

string s = "abc";
s.Replace("a", "z");
Console.WriteLine(s); // Output?
Still prints "abc" – because .Replace() returns a new string, and original is unchanged.



10. String Interning
.NET stores identical string literals in a single memory location to optimize memory.

Interned strings use the same reference.

string s1 = "test";
string s2 = "test";
bool areSame = Object.ReferenceEquals(s1, s2); // true



