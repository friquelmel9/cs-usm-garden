---
{"dg-publish":true,"permalink":"/01-atomic/computer-science/oop-in-c/","tags":["cs/oop","cs/lang/cpp","university/INF201"],"dg-note-properties":{"tags":["cs/oop","cs/lang/cpp","university/INF201"],"source":["https://www.w3schools.com/cpp/cpp_oop.asp"]}}
---

# OOP in C++

This is a list of implementations of [[01-atomic/computer-science/Object-Oriented Programming\|Object-Oriented Programming]] in [[C++\|C++]].
## Classes
[[01-atomic/computer-science/Class\|Class]] are a [[Data Type\|Data Type]] using the `class` keyword
```cpp
class myClass {
	public:
		int attribute; // Attribute
		int method(); // declaration of method
}; // Note the ; in the end, like an struct
```
## Object
An [[01-atomic/computer-science/Object\|Object]] needs the class to be declared beforehand.
```cpp
int main(){
	myClass myObject;
	return 0;
}
```
## Method
A [[01-atomic/computer-science/Method\|Method]] are functions inside the class. 
```cpp
class myClass {
	public:
		int method_inside(int x){ // Implementation outside the class
			return x*2;
		}
		int method_outside(int y); // Declaration of a method
};

int myClass::method_outside(int y){ // Access to the method outside the declaration for the class
	return y/2;
}
```
### Overload
C++ supports [[01-atomic/computer-science/Function Overloading\|Function Overloading]] on methods
```cpp
class myClass {
	public:
		int attribute;
		int method(){ // Method
			attribute++;
		}
		int method(int x){ // Method Overload
			attribute += x;
		}
};
```
### Constructor and Destructor 
C++ supports both [[01-atomic/computer-science/Constructor\|Constructor]] and [[01-atomic/computer-science/Destructor\|Destructor]].
Remember to use [[01-atomic/computer-science/Copy Constructor\|Copy Constructor]] and [[Assignment Operator\|Assignment Operator]] in case of [[Dynamic Memory\|Dynamic Memory]] ([[Rule Of Three\|Rule Of Three]])
```cpp
class myClass {
	public:
		int* attributes;
		
		myClass(){ // Constructor
			attributes = new int[10];
		}
		
		myClass(int x){ // Constructor Overload
			attributes = new int[x];
		}
		
		~myClass(){ // Destructor
			delete[] attributes;
		}
		// Copy constructor
		myClass(const myClass& other) {
		    attributes = new int[10];
		    std::copy(other.attributes, other.attributes + 10, attributes);
		}
		// Copy assignment ooperator
		myClass& operator=(const myClass& other) {
		    if (this != &other) {
		        delete[] attributes;
	        attributes = new int[10];
	        std::copy(other.attributes, other.attributes + 10, attributes);
	    }
	    return *this;
	}
		
};
```


