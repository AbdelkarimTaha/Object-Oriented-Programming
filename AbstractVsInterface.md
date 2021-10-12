An abstract class is a way to achieve the abstraction in C#.
An Abstract class is never intended to be instantiated directly.
This class must contain at least one abstract method, which is marked by the keyword or modifier abstract in the class definition.
The Abstract classes are typically used to define a base class in the class hierarchy.


// C# program to illustrate the
// concept of abstract class
using System;

// abstract class 'G'
public abstract class G {

	// abstract method 'gfg1()'
	public abstract void gfg1();
}

// class 'G' inherit
// in child class 'G1'
public class G1 : G {

	// abstract method 'gfg1()'
	// declare here with
	// 'override' keyword
	public override void gfg1()
	{
		Console.WriteLine("Class name is G1");
	}
}

// class 'G' inherit in
// another child class 'G2'
public class G2 : G {

	// same as the previous class
	public override void gfg1()
	{
		Console.WriteLine("Class name is G2");
	}
}

// Driver Class
public class main_method {

	// Main Method
	public static void Main()
	{

		// 'obj' is object of class
		// 'G' class '
		// G' cannot
		// be instantiate
		G obj;

		// instantiate class 'G1'
		obj = new G1();

		// call 'gfg1()' of class 'G1'
		obj.gfg1();

		// instantiate class 'G2'
		obj = new G2();

		// call 'gfg1()' of class 'G2'
		obj.gfg1();
	}
}

Output :
--------
Class name is G1
Class name is  G2
